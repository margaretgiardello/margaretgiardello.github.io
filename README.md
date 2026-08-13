# Portfolio site — setup notes

## What's in here
- `_site.yml` — nav bar + stock "flatly" theme, no custom CSS
- `index.Rmd` — home page
- `projects.Rmd` — all four projects on one page (section per project)
- `experience.Rmd` — work experience
- `education.Rmd` — education
- `files/` — put `resume.pdf` here

## Before you render
1. Drop your resume PDF into `files/resume.pdf`.
2. In `projects.Rmd`, replace the `TODO` placeholder code chunks with your real
   code, plots, or screenshots. Chunks default to `eval = FALSE` so nothing runs
   until you're ready — flip individual chunks to `eval = TRUE` as you fill them in.
3. Swap the Shiny app link in the Portland Lighting section for your real
   shinyapps.io URL.

## Rendering
From the repo root in R:

```r
rmarkdown::render_site()
```

Outputs to `docs/` (per `output_dir` in `_site.yml`).

## Deploying to GitHub Pages
1. Commit and push, including the `docs/` folder.
2. GitHub repo **Settings > Pages > Build and deployment > Deploy from a branch**.
3. Branch: `main` (or your default), folder: `/docs`.
4. Live in a minute or two at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`.

## Changing the look later
Swap `theme: flatly` in `_site.yml` for another Bootswatch theme — `cosmo`,
`lumen`, `sandstone`, `journal` — no other files need to change.
