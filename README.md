# STAR experiment website

Static Jekyll site replacing the legacy PHP site at www.star.bnl.gov. The structure follows the EICUG site (eicug.github.io): Bootstrap 5, a fixed left sidebar, Markdown pages.

## Run it locally

```bash
bundle config set --local path vendor/bundle   # once
bundle install
bundle exec jekyll serve --livereload          # http://127.0.0.1:4000
```

## How it is organised

| Path | Purpose |
|---|---|
| `_config.yml` | Site title, `url`/`baseurl`, plugins. |
| `_data/navigation.yml` | **The** navigation: drives the sidebar and the Sitemap page. One entry per page. |
| `_data/events.yml` | Meetings on the home page (upcoming/past decided at build time). |
| `_data/related_sites.yml` | BNL/RHIC/DOE links at the bottom of the sidebar. |
| `_posts/` | News items, `YYYY-MM-DD-title.md`. |
| `_layouts/default.html`, `_includes/` | Page template, sidebar, `stub.html` marker. |
| `assets/themes/<theme>/custom.css` | Colours (variables `--star-accent`, `--star-accent-dark`) and content styles. The theme is chosen by `css_theme` in `_config.yml` (`default` = red, `alt` = BNL cerulean/teal). |
| `<section>/<page>/index.md` | One Markdown page per URL. |

## Migrating a page

1. Find the stub: `grep -rl "include stub.html" --include=*.md .` lists everything still to do.
2. Replace the `{% include stub.html ... %}` line with the real content (Markdown or HTML). Copy images to `assets/images/` and link with `{{ '/assets/images/x.png' | relative_url }}`.
3. Keep the `redirect_from:` lines in the front matter. They make the old `www.star.bnl.gov/central/...` address redirect to the new page.
4. Pages with formulas need `math: true` in the front matter.
5. Check it in the local server, then commit.

New page = new folder with `index.md` + one line in `_data/navigation.yml`.

## Conventions

- Phonebook search is gone. The sidebar links to https://phonebook.sdcc.bnl.gov/star/client/ and `/collaboration/phonebook/` redirects there.
- Links to the Drupal site (`drupal.star.bnl.gov`) are kept as external links.
- All internal links use `relative_url`, so changing `url`/`baseurl` in `_config.yml` is all that is needed to move the site.
