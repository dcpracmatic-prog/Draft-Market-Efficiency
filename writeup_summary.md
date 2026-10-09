# Draft Market Efficiency — Write-up Summary (BDB 2027)

## One-sentence claim
Once draft slot is accounted for with a non-linear expectation curve, neither classic Combine metrics, NGS scores, nor 10 Hz drill tracking explain early-career usage residuals out of sample. Observable athleticism acts as an **eligibility filter**, not a continuous upside gradient.

## Stage 1 — Draft slot already prices usage
| Group | N | R² OOF | SD(VOD) |
|-------|--:|-------:|--------:|
| WR | 106 | 0.42 | 198 |
| TE | 42 | 0.53 | 173 |
| CB | 60 | 0.32 | 242 |
| S | 58 | 0.62 | 202 |
| OL | 121 | 0.69 | 223 |
| DL | 88 | 0.47 | 144 |

## Stage 2 — Efficient-market test
**No Supported block.** No pre-draft athletic block has a bootstrap CI for R² that excludes zero after Holm adjustment.

Suggestive only (not Supported): WR/Core Combine (+0.01); TE/Core Combine (+0.01); CB/Tracking COD (+0.03); CB/All athletic (+0.03); S/Core Combine (+0.04); S/NGS (+0.02); OL/NGS (+0.03); DL/NGS (+0.03).

28 / 36 blocks have **negative** OOS R². High-dimensional blocks (All athletic, Tracking magnitude) are systematically negative.

## Filter vs gradient
- corr(athleticism, pick) = **-0.148**
- corr(athleticism, VOD) = **-0.011**
- Interpretation: **Filter-dominant** — athleticism tracks the pick, not residual VOD.

## Implications
1. Treat 1v0 drill athleticism as a threshold for eligibility, not a ranking of residual upside.
2. Marginal value of more resolution on isolated drills is limited once the pick is known.
3. Shift tracking investment toward college game film (11v11).
4. If private EPA/PFF/WAR exist, swap them as Stage-1 targets; pipeline unchanged.

## Methods (one paragraph)
Stage 1: cross-fitted Ridge on spline basis of draft capital + year dummies + undrafted flag → VOD = actual − expected snaps/season. Stage 2: fixed feature blocks (Core/Extended Combine, NGS, Tracking magnitude, Tracking COD, All athletic) predict VOD with leave-one-draft-year-out; bootstrap CI + within-year permutation + Holm. Filter test: PCA-1 of Core Combine vs pick and vs VOD.

## Caveats
Three draft classes; leave-one-year-out; Holm over all Stage-2 tests. LAST_SEASON=2025 and undrafted=300 are assumptions. Snaps measure opportunity, not play quality. Tracking limited to three comparable drills with plausibility filter. Predictive, not causal.

## Headline
Draft slot explains 30–70% of early usage. Nothing in the Combine, NGS, or 10 Hz drill tracking explains the residual out of sample. Athleticism is a filter, not a gradient — the market already priced it.
