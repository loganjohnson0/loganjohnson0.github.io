# loganjohnson0.github.io

Source for [Logan Johnson's personal/academic website](https://loganjohnson0.github.io), built with [Quarto](https://quarto.org).

## Structure

- [`index.qmd`](index.qmd) — home/about page
- [`papers.qmd`](papers.qmd) — publications list
- [`papers/`](papers/) — PDFs of published papers, named `YEAR_JOURNAL_short-slug.pdf`
- [`cv.pdf`](cv.pdf) — current CV, linked from the home page
- `_quarto.yml` — site configuration
- `styles.css`, `serif.scss` — theming

## Developing locally

Requires [Quarto](https://quarto.org/docs/get-started/). To preview the site locally:

```sh
quarto preview
```

To render without previewing:

```sh
quarto render
```

Rendered output goes to `_site/` (gitignored) and is not committed.

## Deployment

The site is published to GitHub Pages via the GitHub Actions workflow at
[`.github/workflows/publish.yml`](.github/workflows/publish.yml). Every push to `main` renders the
site and deploys it automatically — there is no need to render and commit output locally.

For this to work, the repository's **Settings → Pages → Build and deployment → Source** must be
set to **GitHub Actions** (not "Deploy from a branch").

## Adding a new paper

1. Add the PDF to [`papers/`](papers/), named `YEAR_JOURNAL_short-slug.pdf` (e.g.
   `2024_JAS_my-new-paper.pdf`).
2. Add a citation + `[PDF](papers/...)` link entry to [`papers.qmd`](papers.qmd) under the
   appropriate year heading.

## License

Site content is licensed [CC-BY-NC 4.0](LICENSE) unless otherwise noted.
