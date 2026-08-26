# vardhan1303.github.io

Source for my personal portfolio site, built as a static site (no framework,
no build step) so it deploys straight to GitHub Pages.

## Deploy it

1. Create a new **public** repo on GitHub named exactly `vardhan1303.github.io`
   (must match your username, lowercase is fine).
2. Push these files to the `main` branch of that repo:
   ```bash
   cd portfolio
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/Vardhan1303/vardhan1303.github.io.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages** and confirm the source is
   "Deploy from a branch" → `main` / `(root)`. (For a `<username>.github.io`
   repo this is usually already the default.)
4. Give it a minute, then visit `https://vardhan1303.github.io`.

## Before you publish — fill these in

- **Résumé PDF**: export your résumé and save it as
  `assets/Vardhan_Mistry_Resume.pdf` — three buttons on the page link to
  that exact path.
- **Links**: email, LinkedIn and GitHub links are already filled in from
  your public GitHub profile (`mistryvardhan@gmail.com`,
  `linkedin.com/in/vardhan-mistry`). Double-check they're current.
- **Projects**: once your ROS2 computer-vision portfolio project is far
  enough along, swap it in as the flagship project ahead of the thesis card
  — it's a stronger, more direct signal for the drone/SLAM roles you're
  targeting than anything currently on the page.
- **Favicon / OG image**: `assets/favicon.svg` is a placeholder mark — swap
  it for your own if you'd like.

## Structure

```
index.html         one-page site: hero, about, experience, projects, skills, contact
css/style.css       design tokens + layout
js/script.js        mobile nav, scroll reveal, active-link highlighting
media/projects/     real photos pulled from your own repos (platooning.jpg, robot-car.jpg)
media/icons/        tech-stack icons (PyTorch, OpenCV, Docker, etc.) — real SVGs, self-hosted
assets/             favicon + (add your résumé PDF here)
```

No dependencies, no build step, no external image hotlinks — everything the page shows is a local file in this repo. Edit the HTML directly and refresh.

## Company & university logos

IAV, ASAM, Adani, RWU, and MSU Baroda currently show as small monogram badges (IAV, ASAM, AG, RWU, MSU) rather than real logos — I can't fetch files from arbitrary company websites from where I run. If you'd like the real logos instead:

1. Download each one (their press/brand page, or a clean version from Wikimedia Commons) as a small square PNG or SVG.
2. Add them to a new `media/logos/` folder, named e.g. `iav.png`, `asam.png`, `adani.png`, `rwu.png`, `msu.png`.
3. Tell me once they're uploaded and I'll swap the monogram `<div>`s for `<img>` tags pointing at them.


