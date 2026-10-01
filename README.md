# GenomeSpy Blog

The GenomeSpy project blog, built with [Quarto](https://quarto.org/) and intended for \`https://genomespy.app/blog/\`.

## Requirements

- [Quarto](https://quarto.org/docs/get-started/)
- A modern browser for previewing interactive GenomeSpy embeds

## Local development

Preview with live reload:

```sh
quarto preview
```

Build the static site into \`_site/\`:

```sh
quarto render
```

To format Quarto Markdown files, install the pinned Prettier version and run:

```sh
npm ci
npm run format
```

Use `npm run format:check` to check formatting without changing files. The Prettier configuration parses `.qmd` files as Markdown and wraps prose at 80 columns. Review formatted Quarto shortcodes and fenced divs when editing posts.

Create a post by adding a dated `.qmd` file under `posts/`, then copy the front matter from `posts/2026-09-29-genomespy-1-0.qmd`. Quarto supports ordinary Markdown plus code, images, citations, equations, raw HTML, JavaScript, and embedded visualizations.

## Deployment

\`.github/workflows/publish.yml\` renders the site and deploys \`_site/\` with the GitHub Pages deployment actions whenever \`main\` changes. The configured \`site-url\` and relative Quarto links make the generated site work below \`/blog/\`; this repository is independent of both the main GenomeSpy repository and \`genome-spy.github.io\`.

One-time repository setup in GitHub: set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**. The repository must be under the \`genome-spy\` organization, and the \`genomespy.app\` DNS/custom-domain configuration must route \`/blog/\` to this project site as planned by the organization administrators.
