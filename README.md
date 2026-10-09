# NFL Big Data Bowl 2027 — Draft Market Efficiency

![Draft Market Efficiency project image](./image%20(1).jpg)

This repository investigates whether pre-draft athletic measurements explain early-career NFL usage **after accounting for draft position**. The analysis treats snaps as a measure of opportunity, not player quality, and evaluates predictive associations rather than causal effects.

## Main files

| File | Description |
|---|---|
| [`nfl_bdb2027_draft_market_efficiency.ipynb`](./nfl_bdb2027_draft_market_efficiency.ipynb) | Main analysis notebook |
| [`writeup_summary.md`](./writeup_summary.md) | Summary of results, interpretation, methods, and limitations |
| [`WRITEUP_OUTLINE.md`](./WRITEUP_OUTLINE.md) | Proposed structure for the competition write-up |
| [`fig_main.png`](./fig_main.png) | Main analysis figure |
| [`stage1_skill.csv`](./stage1_skill.csv) | Stage 1 out-of-fold draft-position model metrics by position |
| [`stage2_market_test.csv`](./stage2_market_test.csv) | Stage 2 market-efficiency test results |
| [`stage2_suggestive_only.csv`](./stage2_suggestive_only.csv) | Results classified as suggestive, not supported |
| [`filter_vs_gradient.csv`](./filter_vs_gradient.csv) | Athleticism correlations used for the filter-versus-gradient comparison |
| [`ath_terciles.csv`](./ath_terciles.csv) | Athleticism-tercile summary |
| [`players_vod.csv`](./players_vod.csv) | Player-level VOD analysis data |
| [`image (1).jpg`](./image%20(1).jpg) | Repository project image |

The repository also contains `nfl-big-data-bowl.ipynb-7.txt`, an auxiliary text artifact. The executable notebook to start with is `nfl_bdb2027_draft_market_efficiency.ipynb`.

## Research question

Once draft capital is modeled nonlinearly, do pre-draft athletic feature blocks explain variation in early-career usage out of sample?

## Method overview

1. **Stage 1:** Estimate expected snaps per season from draft capital and related draft-year indicators using a flexible, cross-fitted model.
2. **Usage residual:** Define VOD as actual usage minus expected usage. VOD represents opportunity relative to draft-position expectations; it is not a direct measure of player quality.
3. **Stage 2:** Test fixed pre-draft feature blocks using leave-one-draft-year-out evaluation, with bootstrap uncertainty and multiple-testing adjustment.
4. **Filter vs. gradient:** Compare athleticism's association with draft position and with residual usage.

## Current interpretation

The supplied write-up reports that no feature block meets the predefined “Supported” criterion after multiple-testing adjustment. Some results are suggestive, but they should not be presented as confirmed predictive effects. The interpretation is that observable athleticism may operate more as an eligibility/filter signal than as a continuous measure of value beyond draft position.

## Reproduce the analysis

1. Open the main notebook in Kaggle.
2. Attach the official competition dataset and ensure the notebook's expected paths match the attached files. Alternatively, configure `BDB_DATA_DIR` if supported by the notebook.
3. Run the notebook from top to bottom.
4. Inspect the generated outputs and compare them with the committed CSV summaries.

Expected output locations documented by the notebook include `/kaggle/working` or `./outputs_bdb`.

### Dependencies

The documented core dependencies are:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`

Use the versions available in the target Kaggle environment and check the notebook's import/setup cells before running.

## Limitations

- The analysis covers only three draft classes, so leave-one-year-out results provide a limited test of temporal generalization.
- Snaps measure opportunity, not on-field quality.
- The analysis is predictive and observational, not causal.
- Findings should be described as suggestive or unsupported according to the stated statistical criteria; a lack of supported effects is not proof that all athletic information has zero value.

## Project status

The repository contains the main notebook, result summaries, CSV metrics, a figure, and the project image. Verify the notebook by running it against the official competition data before treating the committed results as independently reproduced.
