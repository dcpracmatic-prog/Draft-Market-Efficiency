# NFL Big Data Bowl 2027 — Draft Market Efficiency

## Contents
| File | Description |
|------|-------------|
| `nfl_bdb2027_draft_market_efficiency.ipynb` | Full analysis notebook (run on competition data) |
| `writeup_summary.md` | Results + claim ready for the write-up |
| `thumbnail_560x280.png` | Competition thumbnail |
| `stage1_skill.csv` | Stage 1 R² by position |
| `stage2_suggestive_only.csv` | Only Suggestive Stage-2 cells (0 Supported) |
| `filter_vs_gradient.csv` | Filter vs gradient correlations |
| `ath_terciles.csv` | Athleticism terciles (pick & VOD) |
| `WRITEUP_OUTLINE.md` | Suggested paper structure |

## How to reproduce
1. Attach the official BDB 2027 dataset on Kaggle (or set `BDB_DATA_DIR`).
2. Open the notebook → **Run All**.
3. Outputs land in `/kaggle/working` (or `./outputs_bdb`).

## Dependencies
`numpy`, `pandas`, `matplotlib`, `scikit-learn`

## Claim
Once draft slot is removed with a non-linear expectation, no fixed pre-draft athletic block explains usage residuals out of sample. Athleticism is an eligibility filter, not a value-over-pick gradient.
