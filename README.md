# solarcells

GitHub repository synced to an Overleaf project via GitHub Actions.

## One-time setup

1. Open your Overleaf project and copy the Git project ID (the value after `git.overleaf.com/`).
2. In GitHub repo settings, add these Actions secrets:
   - `OVERLEAF_PROJECT_ID`
   - `OVERLEAF_TOKEN`
3. Use an Overleaf Git authentication token from:
   - Overleaf -> Account Settings -> Git authentication tokens

## Automation behavior

- Workflow file: `.github/workflows/sync-overleaf.yml`
- Triggers on:
  - push to `main` or `master`
  - manual run (`workflow_dispatch`)
- Pushes current GitHub commit to Overleaf `master` branch.

## Notes

- This is a one-way sync: GitHub -> Overleaf.
- If teammates edit directly in Overleaf often, pull those changes into GitHub before further pushes to avoid drift.
