# Troubleshooting

## 1. File Does Not Save

Check:
1. Workspace is open.
2. Folder is writable.
3. File/folder was not deleted externally.

Quick test:
1. Press `Ctrl/Cmd + S`.
2. If needed, use `Ctrl/Cmd + Shift + S` (`Save As`).

## 2. Search Does Not Find Recently Added Text

Try:
1. Wait ~1 second (autosave/index refresh).
2. Close and reopen Search (`Ctrl/Cmd + K`).
3. Confirm file is `.md` or `.txt` for full-text indexing.

Note:
- filename search works for all file types,
- content search is focused on text files.

## 3. Old Name Still Visible After Rename

Usually this resolves automatically after tree refresh.

If stale UI remains:
1. Switch view (`Editor` -> `System Map` -> back),
2. or collapse/expand the affected folder.

## 4. Help/About Links Do Not Open

Check:
1. App is running in normal desktop environment.
2. Default system browser is available.

## 5. Cannot Create File/Folder

Validate name:
- not empty,
- not `.` or `..`,
- no `/` or `\\` characters.

## 6. Analytics Is Empty

Ensure tracker format is correct:
- `$label = current / target`
- example: `$reading = 12 / 30`

Requirements:
- source file should be `.md` or `.txt`.

## 7. System Map Does Not Show Wiki Links

Check syntax:
- `[[FileName]]` or `[[NameWithoutExtension]]`

Also:
- target file must exist in the current Workspace.

## 8. Clean Session Reload

To fully refresh your working session:
1. Click `Back to Hub` in sidebar.
2. Reopen Workspace via `Open Existing`.
3. This rebuilds tree and search index from disk.
