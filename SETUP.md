# 🚀 Setup Instructions

## 1. Copy files to your profile repo

Your GitHub profile repo is: `github.com/KanishkaShukla04/KanishkaShukla04`

Upload everything:
```
KanishkaShukla04/
├── README.md                              ← main profile
├── assets/
│   └── header.svg                         ← animated header
└── .github/
    └── workflows/
        └── update-pinned-repos.yml        ← auto-update pinned repos
```

## 2. Add the GH_TOKEN secret (for pinned repo auto-update)

1. Go to: `github.com/settings/tokens`
2. Generate a **Classic token** with scopes: `repo`, `read:user`
3. Copy the token
4. Go to your profile repo → **Settings** → **Secrets and variables** → **Actions**
5. Click **New repository secret**
6. Name: `GH_TOKEN` | Value: paste your token
7. Save

The workflow runs every 6 hours. You can also trigger it manually from the **Actions** tab.

## 3. Set up Pac-Man contribution graph (optional but impressive)

Add `.github/workflows/pacman.yml` as described in the README's `<details>` block.

The `Platane/snk@v3` action generates a Pac-Man SVG from your contribution graph and pushes it to the `output` branch. The README image URL reads from that branch automatically.

No extra tokens needed — uses `GITHUB_TOKEN` which is built-in.

## 4. Pin your repos on GitHub

Go to your profile → click **Customize your pins** → select up to 6 repos.

The GitHub Action reads these pinned repos via GraphQL and updates the `<!-- PINNED-REPOS:START -->` section in your README every 6 hours automatically.

## 5. Verify everything renders

After pushing, view your profile at:
`https://github.com/KanishkaShukla04`

The SVG header renders inline. All stats cards load from external services — they may take a few seconds on first load.

## Services used (all free, reliable)

| Widget | Service |
|---|---|
| Stats, Top Langs | github-readme-stats.vercel.app |
| Streak | streak-stats.demolab.com |
| Activity graph | github-readme-activity-graph.vercel.app |
| Profile summary cards | github-profile-summary-cards.vercel.app |
| Trophies | github-profile-trophy.vercel.app |
| Visitor counter | komarev.com/ghpvc |
| Footer wave | capsule-render.vercel.app |
| Pac-Man | Platane/snk GitHub Action |
| Pinned repos | Custom GitHub Action (included) |
