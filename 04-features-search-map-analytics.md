# Search, System Map, Analytics

## Search (Command Palette)

Open Search via:
- `Ctrl/Cmd + K`,
- Sidebar -> `Search`,
- top menu -> `Selection` -> `Search`.

Search works on:
- file names,
- file content (`.md`, `.txt`).

Behavior:
- fuzzy matching (tolerates minor typos),
- highlight of matched tokens,
- content snippet around match,
- index refreshes when workspace changes,
- active file content is updated in search index in real time while editing.

## Selecting a Search Result

When selecting a result:
- target file opens,
- app switches to `Editor`,
- query is highlighted in editor,
- editor scrolls to first highlighted match.

## System Map

`System Map` is a graph representation of the Workspace structure.

It shows:
- folder/file nodes,
- hierarchical relations,
- wiki-links from `[[FileName]]` syntax as dashed link edges.

Controls:
- click folder node: expand/collapse,
- click file node: open in Editor,
- zoom/pan supported via React Flow controls.

Wiki-link format:
- write `[[FileName]]` or `[[NameWithoutExtension]]` inside notes,
- if target file exists, a graph link is rendered.

## Analytics

`Analytics` scans markdown/text files for trackers and visualizes progress.

Tracker format:
- `$label = current / target`
- examples:
- `$books = 3 / 12`
- `$sales = 42 / 100`

Behavior:
- single tracker per label -> editable card,
- multiple trackers with same label -> aggregated summary card,
- click single-tracker card -> opens source file,
- value can be edited inline (`Enter` to confirm).

Update behavior:
- refresh button updates analytics data,
- editing a tracker value triggers data recalculation.
