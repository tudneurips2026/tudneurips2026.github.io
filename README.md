# TUD — Project Page

Project page for **TUD: Triggering Generalist Reasoning via Predictive Uncertainty for Dual-System VLA**
(NeurIPS 2026).

Live site: https://tudneurips2026.github.io/

Built from the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template),
matching the layout of our other project pages (VIPS, VR-Drive, HEAT).

## Deploying

`tudneurips2026/tudneurips2026.github.io` is a GitHub organization page, so the repository name matches the domain
and the site is served from the repository root.

Push the contents of this directory to `main`:

```bash
git init -b main
git add .
git commit -m "Add TUD project page"
git remote add origin https://github.com/tudneurips2026/tudneurips2026.github.io.git
git push -u origin main
```

Then, in **Settings → Pages**, set the source to `main` / `/ (root)`. The site goes live at
`https://tudneurips2026.github.io/` within a minute or two.

`.nojekyll` is already present, so GitHub Pages serves the files as-is without running Jekyll.

### Using a different name

If you pick a different organization name, update every occurrence of `tudneurips2026.github.io` in
`index.html` (Open Graph / Twitter / JSON-LD URLs):

```bash
sed -i 's/tudneurips2026\.github\.io/YOURNAME.github.io/g' index.html
```

## Before going public

The **Paper**, **arXiv** and **Code** buttons are currently disabled "Coming Soon" chips, since none of the three
targets exists yet. To turn one back into a working link, replace its
`<span class="button is-normal is-rounded is-coming-soon" ...>` with
`<a href="..." target="_blank" class="external-link button is-normal is-rounded is-dark">`, and drop the
"(Coming Soon)" suffix from the label.

- [ ] Link the Paper and arXiv buttons, and add matching `citation_arxiv_id` / `citation_pdf_url` meta tags.
- [ ] Link the Code button once the repository is public.
- [ ] Remove the "Paper, arXiv & code will be linked here once available" tag once all three are live.
- [ ] Fill in the BibTeX `pages`/`volume` fields once the proceedings entry exists.
- [ ] Add author homepages for Wooseong Jeong and Kuk-Jin Yoon if they have them.

## Layout

```
index.html                           all page content
static/css/                          bulma + template styles (unmodified)
static/js/                           carousel, slider, copy-bibtex, scroll-to-top (unmodified)
static/videos/TUD_demo.mp4           u_t traced through a long-horizon VLA-Arena rollout (H.264 baseline, 8.6 s)
static/images/teaser.png             Fig. 3  — TUD framework (architecture, dispersion, invocation rule)
static/images/motivation_interval.png OpenHelix call-interval sweep on CALVIN
static/images/pareto_*.png           cost-success curves per VLA-Arena domain (L0)
static/images/uncertainty_compare.png signals on success vs. failure rollouts
static/images/scenario_*.png         u_t traced within representative rollouts
static/images/robot_setup.jpg        SO-101 real-robot platform
static/images/favicon*               generated lettermark icons
static/pdfs/                         drop the camera-ready PDF here if you want to host it locally
```

Figures were rendered from the paper's source PDFs at 170 dpi and capped at 1920 px wide; the Pareto plots are the
paper's own PNGs downscaled to 1400 px.

## License

Website content is licensed under
[CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).
