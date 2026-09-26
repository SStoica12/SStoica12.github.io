# Remaining TODOs

These are content placeholders, not build errors. The website works as supplied.

## 1. Add publication figures

The folder is **`assets/images/publications/`**, relative to the repository root.
Each entry already points to its own SVG placeholder. To use a PNG instead:

1. Put your image in that folder, for example `assets/images/publications/mol.png`.
2. In `index.html`, find `id="mol"` and change the image `src` from `assets/images/publications/mol.svg` to `assets/images/publications/mol.png`.
3. Replace its `alt` text with a short description of the real figure. Remove “coming soon.”
4. Delete the unused placeholder if desired. Commit both the image and `index.html`.

**Do not simply rename PNG/JPG bytes to an `.svg` extension.** Use the correct extension in the HTML.
Figures are displayed with `object-fit: contain`, so the entire image remains visible. A landscape figure near 8:5 works well; use at least 640 pixels in width.

| Work | Existing placeholder to replace | HTML entry ID |
| --- | --- | --- |
| Mixture of Layers | `assets/images/publications/mol.svg` | `mol` |
| Feature Recovery | `assets/images/publications/frm.svg` | `frm` |
| PAPO | `assets/images/publications/papo.svg` | `papo` |
| Representation Geometry | `assets/images/publications/geometry.svg` | `geometry` |
| MOF Generation | `assets/images/publications/mof.svg` | `mof` |
| AcquisitionSynthesis | `assets/images/publications/acquisition.svg` | `acquisition` |
| SoundWeaver | `assets/images/publications/soundweaver.svg` | `soundweaver` |
| Stock Prediction | `assets/images/publications/stock.svg` | `stock` |

## 2. Replace missing paper links

Google Scholar returned a rate-limit response; its full paper list could not be checked. Four CV paper URLs were available and used directly. Four others currently open intentionally blank local pages, as requested:

| Entry | Current `href` to replace in `index.html` |
| --- | --- |
| Geometry | `papers/geometry.html` |
| MOF Generation | `papers/mof.html` |
| AcquisitionSynthesis | `papers/acquisition.html` |
| SoundWeaver | `papers/soundweaver.html` |

Replace the `href` with the correct paper URL and change the visible label from `Paper · coming soon` to `Paper`. Remove or update its `aria-label` as well. The blank local file can then be deleted. These placeholder links do not claim that the works were verified on Scholar. Compare the complete list against Scholar when available.

Already populated from the supplied CV:
- MoL: `https://openreview.net/pdf?id=NBGxbQl0VI`
- FRM: `https://arxiv.org/pdf/2609.12078v1`
- PAPO: `https://arxiv.org/pdf/2507.06448`
- Stock prediction: `https://publications.waset.org/10013442.pdf`

## 3. Add code and project websites

PAPO's Website and Code links are already live. For each other publication, replace each relevant `<span class="pending">…</span>` with an anchor when released:

```html
<a href="YOUR_ACTUAL_CODE_URL">Code</a>
<a href="YOUR_ACTUAL_PROJECT_URL">Website</a>
```

The “coming soon” spans are intentionally not links and do not navigate to broken websites.

## 4. Review bio and publication metadata

- The full LinkedIn About text was not publicly retrievable. The draft bio paraphrases its accessible opening and uses only the supplied CV for additional factual detail. Paste the full About text if you want the bio to follow it more closely.
- The CV labels the MOF project “Nature Computational Science” without an explicit acceptance/submission status. To avoid implying acceptance, the page currently displays “Argonne × NVIDIA.” Confirm status before adding the journal venue.
- AcquisitionSynthesis and SoundWeaver use full titles visible on the supplied LinkedIn profile; author lists and current submission destinations follow the CV.
- Confirm the publication author order/asterisks and preferred final titles before any later updates. The supplied author lists were retained.

## 5. Create and publish the remote repository

The files are complete, but GitHub access is not connected in this session. Add/connect GitHub to allow repository creation, or follow `README.md` to create `SStoica12/SStoica12.github.io` and enable Pages.
