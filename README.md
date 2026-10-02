# Theodora Kontogianni — academic website

Source code for [theodorakontogianni.github.io](https://theodorakontogianni.github.io/), Theodora Kontogianni’s academic website.

The site contains research and publication information, teaching, a team page, and academic service and funding updates. It is built with Jekyll and the al-folio theme.

## Updating the site

Most content is maintained in these files:

- `_pages/about.md` — homepage biography and news
- `_pages/team.md` and `_data/team.yml` — team page and profiles
- `_pages/teaching.md` — courses
- `_bibliography/papers.bib` — publications
- `_config.yml` — site title, links, and general settings

Commit and push changes to the `group` branch to publish them. The [deployment workflow](.github/workflows/deploy.yml) installs the site’s dependencies, builds the website, and publishes it to GitHub Pages automatically. Check the repository’s **Actions** tab for the deployment result.

In **Settings → Pages → Build and deployment**, the publishing source should be **GitHub Actions**.

## Theme and license

This website uses [al-folio](https://github.com/alshedivat/al-folio), an academic Jekyll theme. See [LICENSE](LICENSE) for the repository license and theme attribution.
