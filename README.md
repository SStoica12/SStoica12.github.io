# Sofia Stoica — personal website

A self-contained, responsive academic website for `https://sstoica12.github.io/`.
Plain HTML and CSS: no compilation, package installation, external fonts, or JavaScript required.

**Repository prepared locally; it has not been created or published on GitHub yet.**

## Publish on GitHub (browser method)

1. Sign in as **SStoica12** and create a **public** repository named **SStoica12.github.io**. If that repository already exists, review and back up its contents before integrating these files.
2. Unzip this package. Upload the **contents** of `SStoica12.github.io/` to the repository root. `index.html` must be at the root, not inside another folder. Preserve the `assets/` and `papers/` folders. There is intentionally no `CNAME` file.
3. Commit the files to `main`.
4. Open **Settings → Pages**. Choose **Deploy from a branch**, then **main** and **/(root)**, and save.
5. Wait for the Pages deployment to complete. Visit `https://sstoica12.github.io/`.

If a custom domain is configured on an existing repository, clear it to use the GitHub Pages URL.

## Publish with Git and the GitHub CLI

After installing Git and the GitHub CLI, open a terminal **inside the extracted website folder**:

```bash
gh auth login
git init -b main
git add .
git commit -m "Create Sofia Stoica personal website"
gh repo create SStoica12/SStoica12.github.io --public --source=. --remote=origin --push
```

Use this command only for a **new** repository. Then enable Pages using step 4 above.
No force push or deletion is needed.

## Preview and edit

Open `index.html` in your browser. Alternatively, run the following inside the website folder:

```bash
python3 -m http.server 8000
```

Visit `http://localhost:8000`. Edit `index.html` and `styles.css`, save, and refresh.
After publication, commit and push edits to `main`; GitHub Pages will redeploy.

## File guide

| File or folder | Purpose |
| --- | --- |
| `index.html` | Bio, contact links, two updates, all eight publication entries, and reference credit |
| `styles.css` | Times New Roman, blue palette, spacing, desktop/mobile layouts |
| `assets/images/profile.jpg` | Your supplied `IMG_2378.jpg`, copied without alteration |
| `assets/images/publications/` | Eight individual publication figure placeholders |
| `assets/favicon.svg` | Simple blue “S” browser-tab icon |
| `papers/` | Four intentionally blank destinations for missing paper URLs |
| `.nojekyll` | Tells GitHub Pages to serve the static files directly |
| `TODO.md` | Remaining content/figure/link tasks and all exact paths |
| `SOURCES.md` | Content sources, reference credit, and source limitations |

## Where the requested changes were made

Search for **UPDATED** or **TODO** in the source. Comment numbers correspond to your request:

1. **Times New Roman:** `styles.css`, `body` font-family (headings and links inherit it).
2. **Blue instead of purple:** `styles.css`, `:root`, anchors and visited anchors. Light-blue surfaces and a readable blue for small text; no purple states.
3. **Bio:** `index.html`, `.biography`, based on the accessible LinkedIn opening and the supplied CV. Full LinkedIn About text was unavailable; this is explicitly flagged for review.
4. **Contact links:** `index.html`, `.contacts`, only below the photo. LinkedIn, Google Scholar, GitHub, and email exactly as provided.
5. **No additional social accounts:** no Twitter, Instagram, Substack, or other social links.
6. **Two updates:** `index.html`, `.updates`; September 24 and January 25, 2026. PAPO metrics are supported by the supplied LinkedIn profile's announcement and project page.
7. **All research works:** eight `.publication` entries; real paper links from the CV; PAPO website/code; image placeholders and missing-resource comments per entry.
8. **Profile photo:** `assets/images/profile.jpg`, referenced by `.portrait`.
9. **Reference credit:** visible footer links to Sophia Tang’s website; further attribution in `SOURCES.md`. Original HTML/CSS, not a source-code fork.

No phone number, grades, invented accomplishments, or unsupported publication acceptances were added. The provided CV is used as a source, not published as a downloadable file.

## Validation completed

- All local image, stylesheet, favicon, paper-placeholder, and in-page anchor paths resolve.
- Confirmed eight publication entries, exactly two updates, and nine images with alt text.
- Confirmed all four contact links are only beneath the profile photo.
- Confirmed profile image matches the supplied original byte-for-byte.
- Responsive CSS is included for desktop, tablet, and mobile. A browser rendering check could not be completed in the authoring environment because its browser runtime could not be installed. Preview locally before publishing.
