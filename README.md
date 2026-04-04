# Ellis & Messina — Update Repository

This repository holds the auto-update files for the **Ellis & Messina Micropaleontology Search** app.

## Files

| File | Purpose |
|------|---------|
| `version.txt` | Current version string (YYYY.MM.DD) |
| `Update_Ellis_Messina.zip` | Code-only update package (~2-3 MB) |

## How it works

When users launch the app via `Ellis_Messina.bat` (Windows) or `Ellis_Messina.command` (Mac), the launcher:
1. Fetches `version.txt` from this repo
2. Compares it to the local version
3. If newer: downloads `Update_Ellis_Messina.zip`, extracts it, and relaunches

## Publishing an update

From the main project root:
```bash
bash deploy/github/push_update.sh
```

This bumps the version, builds the zip, and pushes here automatically.
