# GhostFS

GhostFS keeps a live copy of a project folder and restores it to the latest copied state.

## Install

Install once for your Windows user so the `ghost` command is available in every project:

```cmd
git clone https://github.com/pixrog/ghostfs
cd ghostfs
pip install -e .
```

## Start a live save

From the project directory, run `ghost init`, enter a save name, and leave the command running. GhostFS stores the copy under `C:\GhostFS\saves\<save-name>\` and syncs file changes automatically. Press Ctrl+C to stop watching; run `ghost init` again to resume the existing save (choose a new name only after removing the old save).

## Restore

Run `ghost undo C:\MyProject` from any directory. GhostFS replaces the target folder's contents with its latest live save.

By default data is stored in `C:\GhostFS`. Set `GHOSTFS_HOME` before launching GhostFS to use a different storage directory.
