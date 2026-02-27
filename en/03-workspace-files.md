# Workspace, Files, Folders

## Workspace Concept

A `Workspace` is the root project folder in your active session.

Key rules:
- One active Workspace at a time.
- App stores recent Workspaces (`Recent Locations`).
- You can remove a Workspace from recent list without deleting files from disk.

## Single Selection Model

QUANTA uses single selection:
- if a file is selected, only that file is active;
- if a folder is selected, only that folder is active.

This is important for correct create behavior.

## Create Target Logic

When you click `New File` or `New Folder`, the target is resolved as:
1. If a folder is selected: create inside that folder.
2. If a file is selected: create in that file's parent directory.
3. Otherwise: create in Workspace root.

## File Creation

On creation:
- `.md` extension is auto-added if missing,
- initial content uses `# FileName` header,
- new file is opened automatically,
- cursor is focused in the editor so you can type immediately.

## Rename

Rename works for both files and folders.

What updates immediately:
- tree label,
- internal path,
- active editor file path (if renamed item is open),
- selected folder path,
- workspace/search structures after refresh.

Name restrictions:
- name only (not a full path),
- cannot be empty, `.` or `..`,
- cannot contain `/` or `\\`.

## Context Menu (Right Click)

On file/folder:
- `Rename`
- `Copy`
- `Cut`
- `Delete`
- for folders additionally:
- `New File Inside`
- `New Folder Inside`
- `Paste` (when clipboard has data)

On empty tree area:
- `Paste Here`
- `New File`
- `New Folder`

## Drag and Drop

You can drag files/folders into another folder:
- operation is performed as `move`,
- workspace tree refreshes after move.

## Autosave and Manual Save

- Editor changes are autosaved.
- Manual save: `Ctrl/Cmd + S`.
- `Save As` creates a new file in chosen path and sets it active.

## Draft / Inbox

The app maintains a built-in draft file (`draft.md`) under `Documents/Quanta`.

Flow:
- write in Draft,
- click `Save Note`,
- note is saved into the current Workspace.
