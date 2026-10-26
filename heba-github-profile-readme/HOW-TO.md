# Update your profile README — how to apply this

I did not push anything to GitHub for you. Copy these two files into your
special profile repo (the repo named exactly `hebaalazzeh`):

1. `README.md` → repo root, replacing the current `README.md`
2. `info-card.svg` → `.github/assets/info-card.svg`

Your existing readme-aura files in `.github/assets/` stay untouched — the
new README still points at components 0–10 exactly as before.

## Check before you commit

```bash
pwd
ls
git status
```

Make sure `pwd` ends in just one `hebaalazzeh` folder, and that `git status`
shows only `README.md` and `.github/assets/info-card.svg` as changed/added.

## Commit (normal push, no force)

```bash
git add README.md .github/assets/info-card.svg
git commit -m "Add profile views counter and animated neofetch card"
git push
```

## What changed, and why it works this way

- **Profile views counter:** the Komarev badge at the top.
  Honest limit: it counts loads of the badge, not true unique GitHub
  profile visitors — a counter needs a hosted service to count, so it
  can't be fully self-hosted the way Avi's SVGs are. If Komarev is ever
  down, only that badge breaks, not the rest of the page.
- **Terminal framing:** `$ whoami` / `$ neofetch` headings, in the style
  of Avi Vashishta's post. GitHub strips `<script>` and almost all inline
  CSS from READMEs, so the animation itself has to live *inside* the SVG
  — that's why `info-card.svg` uses SMIL fades (one line at a time)
  instead of markdown/CSS animation.
- **Live contribution heatmap (optional, commented out in README.md):**
  follow Avi's post — scrape your public contributions page (no token
  needed), render it as an animated SVG, and refresh it daily with a
  GitHub Actions cron. Only uncomment that block in README.md once
  `contrib-heatmap.svg` actually exists in `.github/assets/`, or it
  will show as a broken image. Same idea for his ASCII portrait: it
  needs a photo run through his prep/convert scripts first, so I didn't
  invent one for you.

Source post: https://www.avivashishta.com/blog/build-animated-github-profile-readme
