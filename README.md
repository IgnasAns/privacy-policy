# privacy-policy

Public privacy-policy page for the ten IA Engineering offline mobile games.
Served at **https://ignasans.github.io/privacy-policy/** once published — that URL is the
privacy-policy field for every one of the ten Play Console app records.

- Publisher: **IA Engineering**
- Privacy contact: **info@iaengineering.net**
- Effective date: **23 September 2026**

## Publish (one time)

```bat
cd /d C:\Users\Ignas\Documents\ChatGPT\Testers\mobile-game-portfolio\privacy-policy
git init
git add .
git commit -m "Privacy policies for the ten portfolio games (effective 2026-09-23)"
gh repo create privacy-policy --public --source=. --push
gh api repos/IgnasAns/privacy-policy/pages -X POST -f "source[branch]=main" -f "source[path]=/"
```

(Or create the public repo `privacy-policy` under **IgnasAns** in the GitHub web UI and set
Settings → Pages → Deploy from a branch → `main` / `(root)`.)

Then verify https://ignasans.github.io/privacy-policy/ loads before entering the URL in
Play Console.

## Keep in sync

`index.html` mirrors the in-app notice at `games/<game>/web/privacy.html` and the
listing copy at `games/<game>/store-listing/privacy-policy.md`. If data practices change,
update all three places together and bump the effective date everywhere.
