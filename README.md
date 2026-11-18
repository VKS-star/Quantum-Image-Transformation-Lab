# Quantum Image Transformation Lab — supplied 12-image dataset

The existing notebook layout, inline FRQI implementation, original upload/Compare controls, MNIST study, folder-access fix, and Section 12A recovery comparison are preserved. The photo dataset is now exactly the 12 images supplied in this chat. The previous sunset, stock-photo collection, and simulated exposure variants are excluded.

## Run

Extract the entire ZIP and keep `data/` beside the notebook. Use Python 3.11–3.13:

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter notebook Quantum_Image_Transformation_Lab.ipynb
```

On Windows activate with `.venv\Scripts\activate`. Restart the notebook kernel and run all cells. Dependencies need installation once; the included 12 photos and actual MNIST archive need no download. The HTML copy is a static view of the executed results; its upload controls need a live notebook.

If Jupyter's current directory is inaccessible, the first cell checks standard named project folders and validates this dataset's manifest before selecting a folder. You can set `PROJECT_DIR` in that cell to an absolute path. If macOS denies access to the folder itself, move the entire extracted folder in Finder to `~/Quantum_Image_Transformation_Lab`, restart Jupyter, and rerun. Code does not override macOS permissions.

## Dataset and coverage

`data/photos/` contains all 12 original JPEG attachments under their original filenames, with unchanged bytes. `data/dataset_manifest.json` records their order, dimensions, source filenames, SHA-256 checksums, source brightness, and individual notes. They are user-provided images; their original creators, licenses, capture settings, and independent capture authenticity were not verified. No normal-light ground-truth pair is invented.

Images 1–6 show cave scenes, 7–10 show dim indoor/outdoor/night scenes, and 11–12 show strong light trails or sunlight glare. All are included as requested, even though the last two are not uniformly low-light inputs. Some sources already have haze or shallow focus. Brightness processing does not deblur them; no artificial blur or exposure degradation is added.

All 12 inputs are used in:

- Section 11: originals, 8×8/16×16 brightness benchmarks, and classical/quantum negatives.
- Section 12: original-versus-transformed galleries at +10%, +25%, +50%.
- Section 12A: transform/reconstruct/recover comparisons at 32×32, including classical, exact quantum, and finite-shot quantum methods for all three increases and the negative.

Section 14 uses the first supplied cave image for its original finite-shot study. Section 9 retains the separate required 20 actual MNIST test images at 4×4 and 8×8. The original optional LOL section remains but is skipped when not supplied; it does not replace these 12 inputs. The upload interface can still test a selected image separately.

`results/` contains benchmark CSVs, 12 photo galleries, and 48 recovery comparison figures with floating-point arrays and quality metrics. Figure panels use the original grayscale grid as their reference; full-resolution originals are also shown in Section 11. FRQI outputs are small grayscale reconstructions, not full-resolution color quantum processing.

## Interpretation

Only brightness **increases of 10%, 25%, and 50%** are tested; each starts independently from its original. The negative comparison remains the separately requested X-gate operation. Global Ry remains the original additive demonstration and can wrap; controlled multiplication is the primary matching classical comparison. No darkening condition or automatic exposure correction is introduced.

Classical and ideal quantum controlled transformations should agree within numerical precision; finite-shot quantum readout adds error. Recovering the original after clipped brightening cannot restore lost highlights, especially in the brighter supplied images. Recovery uses decoded transformed pixels and the known gain, not saved original angles. Recovery metrics and forward-operation agreement are separate; neither measures restoration to a missing normal-exposure reference. No universal quality improvement, deblurring, hardware execution, or end-to-end quantum speedup is claimed.
