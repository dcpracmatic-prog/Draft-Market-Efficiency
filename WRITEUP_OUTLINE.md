# Write-up outline (competition submission)

1. **Introduction** — Is there undiscovered alpha in pre-draft drill tracking after the market sets a pick?
2. **Data** — Official BDB files; PLAYER-only tracking; three drills; plausibility filter; fine positions (WR, TE, CB, S, OL, DL).
3. **Methods**
   - Stage 1: spline E[snaps/season | pick, year] → VOD (cross-fitted).
   - Stage 2: fixed blocks → VOD, leave-one-draft-year-out, bootstrap + Holm.
   - Filter vs gradient: PCA athleticism vs pick and vs VOD.
4. **Results** — Stage-1 table; Stage-2 (0 Supported, 28/36 negative R²); filter-dominant correlations; main figure.
5. **Discussion** — Efficient draft market for observable athleticism; drills as eligibility filter; recommend 11v11 college tracking.
6. **Limitations** — Volume ≠ quality; short careers; three classes; no EPA/PFF in public data.
7. **Appendix** — Feature definitions, audit, full Stage-2 CSV from notebook export.
