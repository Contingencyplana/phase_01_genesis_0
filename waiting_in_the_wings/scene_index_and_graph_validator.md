# Scene Index and Graph Validator

## Ten-Line Scene Index System and Scene Graph Validator

Since your runtime successfully navigated scenes like `0001 → 0101 → 0301 → 0302`, the loader and parser are working. The crash you saw earlier was just a missing scene file, which you fixed. So the engine is functionally correct.

Right now the loader finds scenes using:

```python
scenes_root.rglob(expected_name)
```

That means every time a scene loads, Python searches the entire `story/scenes/` tree.

With 22 scenes this is instant.  
With 2,000 scenes, it becomes noticeably slower.

The fix is simple: build a scene index once at startup, then look up scenes in constant time.

## The 10-Line Scene Index System

Create a small index builder inside `scene_loader.py`.

```python
from pathlib import Path

def build_scene_index(scenes_root: Path) -> dict[str, Path]:
    index = {}
    for path in scenes_root.rglob("scene_*.md"):
        scene_id = path.stem
        index[scene_id] = path
    return index
```

That is the core idea.

This runs once when the engine starts.

## Then Use the Index for Loading

Instead of searching every time:

```python
scene_path = _find_scene_file(scene_id, scenes_root)
```

You use the index:

```python
SCENE_INDEX = build_scene_index(SCENES_ROOT)

def load_scene(scene_id: str):
    path = SCENE_INDEX.get(scene_id)
    if path is None:
        raise FileNotFoundError(f"Scene not found: {scene_id}")
    return parse_scene_file(path)

```

Now loading a scene is:

```text
dictionary lookup → parse file
```

instead of:

```text
recursive filesystem search → parse file
```

Why This Matters

Current runtime behavior:

```text
load_scene()
    ↓
scan entire directory tree
    ↓
find file
    ↓
parse
```

With indexing:

```text
startup
↓
scan tree once
↓
build dictionary

runtime
↓
dictionary lookup
↓
parse
```

So performance becomes:

- `O(n)` startup
- `O(1)` scene lookup

This easily scales to 10,000+ scenes.

## Why This Fits Your Architecture Perfectly

Your scene IDs already follow a strict rule:

- `scene_0001`
- `scene_0204`
- `scene_0302`

So indexing is trivial:

```text
scene_id → file_path
```

Your arc folders (`0000_start`, `0200_library`, and so on) remain purely organizational.

The engine does not care where the file lives.

## Resulting Performance

Approximate lookup times:

| Scenes | Current Loader | Indexed Loader |
|---|---|---|
| 20 | instant | instant |
| 200 | noticeable | instant |
| 2,000 | slow | instant |
| 20,000 | painful | still fast |

## Bonus Benefit

Once you have an index, you can also easily add tools like:

- graph validator
- missing scenes
- dead links
- unreachable scenes

Example:

```text
scene_0302 → scene_0303
scene_0303 missing
```

These become very easy to detect.

## Important Recommendation

Do not implement this immediately.

Your project is still in proto-engine stage.

Best practice:

### Phase 1

- small runtime
- write scenes
- test story graph

### Phase 2

- add indexing
- add graph validator

So, keep the current system for now.

## Later

When you are ready, a small **Scene Graph Validator** would likely be very useful.

A short validator that automatically checks all scenes for broken links before you run the game could save large amounts of debugging time once you reach 100+ scenes.
