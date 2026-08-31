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

Create a post by adding a dated \`.qmd\` file under \`posts/\`, then copy the front matter from \`posts/2026-08-31-example-draft.qmd\`. Quarto supports ordinary Markdown plus code, images, citations, equations, raw HTML, JavaScript, and embedded visualizations.

## Deployment

\`.github/workflows/publish.yml\` renders the site and deploys \`_site/\` with the GitHub Pages deployment actions whenever \`main\` changes. The configured \`site-url\` and relative Quarto links make the generated site work below \`/blog/\`; this repository is independent of both the main GenomeSpy repository and \`genome-spy.github.io\`.

One-time repository setup in GitHub: set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**. The repository must be under the \`genome-spy\` organization, and the \`genomespy.app\` DNS/custom-domain configuration must route \`/blog/\` to this project site as planned by the organization administrators.

The example post is deliberately marked as a draft in its title and categories. Remove it when the first real article is ready.
