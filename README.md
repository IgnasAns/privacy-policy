# privacy-policy

Public privacy-policy page for the ten IA Engineering offline mobile games.
Live at **https://ignasans.github.io/privacy-policy/** (HTTP 200, verified 23 September 2026)
— that URL is the privacy-policy field for every one of the ten Play Console app records.

- Publisher: **IA Engineering**
- Privacy contact: **info@iaengineering.net**
- Effective date: **23 September 2026**

## Clarification published 4 October 2026

Commit `1087b53` clarifies that Lantern Table accepts local, session-only clues;
it offers no online chat or online content sharing. Player labels are generated
(`Player 1`, etc.), rather than personal names entered by players. The data practices
and effective date have not changed. The corrected page was verified live in Brave.

The existing public repository had been archived and Pages was disabled. Publication
restored the repository and its previous `main` / `(root)` Pages source. Repository
visibility remains public and no access permissions or credentials were changed.

## Published (23 September 2026)

Repo: **https://github.com/IgnasAns/privacy-policy** (public), Pages deployed from branch
`main` / `(root)`. The commands used:

```bat
cd /d C:\Users\Ignas\Documents\ChatGPT\Testers\mobile-game-portfolio\privacy-policy
git init
git branch -M main
git add .
git -c user.name=IgnasAns -c user.email=IgnasAns@users.noreply.github.com commit -m "Privacy policies for the ten portfolio games (effective 2026-09-23)"
gh repo create privacy-policy --public --source=. --push
gh api repos/IgnasAns/privacy-policy/pages -X POST -f "source[branch]=main" -f "source[path]=/"
```

(The machine's global git config has no `user.name`/`user.email`, hence the `-c` flags on
the commit; the noreply address keeps the public commit free of a personal address.)

To rebuild elsewhere (e.g. after deleting the repo), run the same commands, then verify
https://ignasans.github.io/privacy-policy/ loads before entering the URL in Play Console.

## Keep in sync

`index.html` mirrors the in-app notice at `games/<game>/web/privacy.html` and the
listing copy at `games/<game>/store-listing/privacy-policy.md`. If data practices change,
update all three places together and bump the effective date everywhere.
