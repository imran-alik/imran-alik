# Publish GitHub Profile README

GitHub shows `README.md` from a **public repo named exactly like your username**: `imran-alik/imran-alik`.

That README renders on **[github.com/imran-alik](https://github.com/imran-alik)** (your profile front page), **not** inside Settings. The repo still exists in the background — that is normal.

**Requirements:** public repo · name = username · `README.md` on default branch **`main`**.

## Files

| File | Purpose |
|---|---|
| [`README.md`](README.md) | Profile content (copy to the special repo) |
| [`SETUP.md`](SETUP.md) | This guide |

## Option A — GitHub web UI

1. Go to [github.com/new](https://github.com/new)
2. Repository name: **`imran-alik`** (must match username exactly)
3. Public · add README → Create
4. Replace default README with contents of [`README.md`](README.md)
5. Commit to `main`

Profile updates in ~1 minute at [github.com/imran-alik](https://github.com/imran-alik).

## Option B — CLI

```powershell
cd C:\Users\imran\Documents\Projects\parent\cv\github-profile
git init
git add README.md
git commit -m "Add profile README — DE portfolio front page"
gh repo create imran-alik --public --source=. --remote=origin --push
```

If the repo already exists:

```powershell
git remote add origin https://github.com/imran-alik/imran-alik.git
git branch -M main
git push -u origin main
```

## Pin repositories

On [github.com/imran-alik?tab=repositories](https://github.com/imran-alik?tab=repositories):

1. **Customize your pins**
2. Pin: `checkout-telemetry-case-study` (and others when public)

Suggested pin description for checkout repo:

> Real-time cart abandonment · 400/400 certified ingest · 10 recovery triggers · GCP stream pattern

## Refresh after project changes

When certification stats change (e.g. new `run_summary_*.json`), update the **Projects in play** table in `README.md` and push.

## Preview locally

Open `README.md` in VS Code/Cursor Markdown preview, or paste into [github.com/imran-alik/imran-alik](https://github.com/imran-alik) after publish.
