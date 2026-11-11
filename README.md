# singhpraveenk.github.io

Source code for the academic website of **Praveen Kumar Singh, PhD**, Postdoctoral Research Scientist at the Laboratoire de Météorologie Dynamique (LMD-IPSL), École Polytechnique, France.

**Live site:** <https://singhpraveenk.github.io>

The site presents research on black carbon, air quality, climate and the cryosphere of the Hindu Kush Himalaya and South Asia, together with publications, talks, media coverage, expeditions and a CV. It is built with [Quarto](https://quarto.org) and hosted on GitHub Pages.

## Site structure

| Folder / file | What it contains |
|---|---|
| `index.qmd` | Home page |
| `about/` | About page and portrait (`profile.jpg`) |
| `research/` | Research themes, one sub-folder per theme |
| `publications/` | One sub-folder per paper: `index.qmd`, key figure, and PDF where the licence allows |
| `talks/` | One sub-folder per talk: `index.qmd`, cover image and slides PDF |
| `news/` | Media coverage, one sub-folder per article |
| `expeditions/` | Field expeditions with photo galleries |
| `cv/` | CV web page and the public PDF (`Praveen_Kumar_Singh_CV.pdf`) |
| `privacy/`, `license/` | Privacy and cookie notice; licence terms |
| `404.qmd` | Custom "page not found" page (uses absolute links so it works at any missing address) |
| `assets/` | Theme SCSS (light and dark), CSS, and self-hosted open-source fonts |
| `assets/footer.css` | Styles for the multi-column site footer (its HTML is under `page-footer` in `_quarto.yml`) |
| `includes/person-schema.html` | Schema.org `Person` data (ORCID, Scopus, Web of Science, etc.) for search engines |
| `_partials/` | Custom title-block template (banner image and link buttons) |
| `_extensions/` | Quarto extensions (see below) |
| `_quarto.yml` | Site configuration: navigation, footer, SEO, analytics and cookie consent |
| `papers.bib`, `generate_publications.py` | Bibliography and a helper script that builds a publication list from it |
| `robots.txt`, `favicon.*`, `apple-touch-icon.png` | Search-engine and browser files copied to the site root |
| `cleanup-unused-files.ps1` | Moves files no page uses out of the repository (nothing is deleted) |

## Building and publishing

Requirements: [Quarto](https://quarto.org/docs/get-started/) 1.4 or later.

```bash
quarto preview            # live preview while editing
quarto render             # build the site into _site/
quarto publish gh-pages   # build and publish to GitHub Pages
```

## Adding content

**A publication.** Create `publications/YYYY_MM_journal/index.qmd`. Copy the front matter of an existing paper and keep:

- `title`, `author` (your entry with `orcid:`), and `date`;
- `venue:`, the journal name shown under the title;
- `description:`, a one-line plain-language summary (≤160 characters) used by search engines;
- `citation:` with `container-title`, `volume`, `page` and `doi`, which produce the Google Scholar meta tags;
- optionally `image: key-figure.jpg` with `image-alt:`, and a PDF button under `links:` plus `resources:`. Only host a PDF if the paper is open access or the publisher allows it.

**A talk or news item.** Copy an existing folder in `talks/` or `news/` and edit the front matter. Add `image-alt:` for every `image:`.

**Images.** Use JPEG for photos, no wider than about 1,400–1,920 px. Add `loading="lazy"` to gallery images below the top of the page.

## Extensions

| Extension | Used for |
|---|---|
| [`quarto-ext/fontawesome`](https://github.com/quarto-ext/fontawesome) | Font Awesome icons (`{{< fa … >}}`) |
| [`schochastics/academicons`](https://github.com/schochastics/academicons) | Academic icons: ORCID, Scopus, Google Scholar, etc. (`{{< ai … >}}`) |
| [`mcanouil/iconify`](https://github.com/mcanouil/quarto-iconify) | Iconify icons |
| [`mvuorre/gallery`](https://github.com/mvuorre/quarto-gallery) | Photo gallery layouts |
| `produnis/publicationlist` | Publication list template |

Each extension keeps its own licence.

## Fonts

The site uses **only open-source fonts**, self-hosted in `assets/fonts/` and declared in `assets/fonts.scss`:

| Font | Used for | Licence |
|---|---|---|
| Petrona | Headings | SIL Open Font License 1.1 |
| Red Hat Text | Body text | SIL Open Font License 1.1 |
| Red Hat Mono | Code | SIL Open Font License 1.1 |
| Tiro Devanagari Hindi | Hindi (Devanagari) text | SIL Open Font License 1.1 |

Icons come from Font Awesome Free and Academicons (SIL OFL 1.1) and Bootstrap Icons (MIT). Font stacks in `assets/theme-*.scss` end in generic families (`serif`, `sans-serif`, `monospace`) rather than proprietary system fonts. Please keep it that way when adding fonts.

## Analytics and privacy

Google Tag Manager (`GTM-WB387NF3`) is loaded **only after a visitor accepts cookies**, through Quarto's built-in cookie consent (`cookie-consent` in `_quarto.yml`, type `express`). The banner wording is replaced by a short script in `_quarto.yml`; the full notice is at [`/privacy/`](https://singhpraveenk.github.io/privacy/).

## Licence

- **Code** (Quarto configuration, templates, SCSS/CSS, scripts): [MIT License](LICENSE).
- **Original text** written by Praveen Kumar Singh: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- **Photographs and personal images:** © Praveen Kumar Singh, all rights reserved.
- **Papers, slides, figures and other third-party material** keep their original licences, stated on each page.

## Contact

Praveen Kumar Singh · [praveenglaciology@gmail.com](mailto:praveenglaciology@gmail.com) · [ORCID 0000-0001-7173-5539](https://orcid.org/0000-0001-7173-5539)
