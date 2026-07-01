# Rall's Hermes Agent fork

This fork exists so Rall can safely inspect, customize, test, and contribute to Hermes Agent without touching the live installed copy or losing the connection to upstream NousResearch.

## What this gives us

- A clean GitHub fork under `recursiverall/hermes-agent`.
- A local development clone at `C:/Users/recur/repos/hermes-agent`.
- A professional remote layout:
  - `origin` → Rall's fork
  - `upstream` → NousResearch canonical repo
- A place for feature branches, experiments, fixes, issues, and pull requests.
- A clean boundary between runtime secrets/config and tracked source code.

## Current setup branch

This file lives on `rall/workspace-bootstrap`, a Rall-specific setup branch. The fork's `main` should stay clean and easy to fast-forward from upstream.

## Useful commands

```bash
cd C:/Users/recur/repos/hermes-agent

# Check where we are
git status
git remote -v

# Sync from upstream
git fetch upstream --prune
git checkout main
git merge --ff-only upstream/main
git push origin main

# Start work
git checkout -b rall/my-change
```

## Important safety rule

Never commit local Hermes runtime files, tokens, `.env`, session logs, profile data, or credentials. Keep the repo for source and documented workflows only.
