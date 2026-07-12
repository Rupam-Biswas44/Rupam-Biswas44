# RupamOS v3.2 — GitHub Profile Setup Guide

## What you got

```
RupamOS-GitHub-Profile/
├── README.md                          ← Your main profile file
├── assets/
│   ├── terminal.svg                   ← The animated terminal (centerpiece)
│   └── typing.svg                     ← Typing subtitle
└── .github/
    └── workflows/
        └── snake.yml                  ← Auto snake animation
```

---

## Step 1 — Create your GitHub profile repo

1. Go to **https://github.com/new**
2. Set the repository name to **exactly your GitHub username**
   - Example: if your username is `Rupam-Biswas44`, name the repo `Rupam-Biswas44`
3. Make it **Public**
4. Do **NOT** add any README (we have our own)
5. Click **Create repository**

---

## Step 2 — Upload all files

Copy the entire folder to GitHub:

```bash
# In your terminal, go to the project folder
cd /Users/rupambiswas/.gemini/antigravity-ide/scratch/RupamOS-GitHub-Profile

# Initialize git
git init
git add .
git commit -m "feat: RupamOS v3.2 profile"

# Add your GitHub repo as remote (replace with your actual username)
git remote add origin https://github.com/Rupam-Biswas44/Rupam-Biswas44.git
git branch -M main
git push -u origin main
```

---

## Step 3 — Enable GitHub Actions (for Snake)

1. Go to your repo → **Settings** → **Actions** → **General**
2. Set "Workflow permissions" to **Read and write permissions**
3. Click Save
4. Go to **Actions** tab → click on "Generate Snake Animation" → click **Run workflow**
5. Wait ~2 minutes, then refresh your profile

---

## Step 4 — Update links in README.md

Open `README.md` and update:

| Placeholder | Your actual value |
|---|---|
| `Rupam-Biswas44` | Your GitHub username |
| `rupam@example.com` | Your actual email |
| `rupambiswas.dev` | Your portfolio URL (or remove) |
| LinkedIn URL | Your LinkedIn profile |
| Project repo links | Your actual repo links |

---

## Step 5 — Verify it looks good

Visit `https://github.com/YOUR-USERNAME` and you should see the animated terminal.

---

## Troubleshooting

**Terminal SVG not showing?**
- Make sure the `assets/` folder was uploaded
- The path `./assets/terminal.svg` must match exactly

**Snake not working?**
- Go to Actions → Enable workflows
- Run the snake workflow manually first

**Stats showing "not found"?**
- Your GitHub username must be exactly `Rupam-Biswas44`
- Stats services may take a few minutes to load

---

## What's animated

| Feature | How it works |
|---|---|
| Boot sequence | SVG `animate` fade in/out |
| Moving scan line | SVG `animateTransform` |
| CRT flicker | SVG `animate` on fill color |
| Glowing border | SVG `animate` on opacity |
| Skill bars | SVG `animate` on width |
| Cursor blink | SVG `animate` on opacity |
| Traffic lights | SVG `animate` on opacity |
| Snake | GitHub Actions + SVG |

All animations are **pure SVG** — no JavaScript needed. GitHub renders them perfectly.
