# What changed in the August 2026 revision

**Short version.** A bug in the panel construction meant every mineral's
treatment group was silently cut down to the cells that also had a copper
discovery. Fixing it changed the treated sample for every result in the paper.
Most of the argument survives. One hypothesis does not, and the tantalum
mechanism reverses.

## The bug

`02_multiscale_panel_construction.R` line 205 built treatment timing with

```r
treatment_timing <- reduce(treatment_list, left_join, by = "hex_id")
```

`reduce` folds `left_join` over the per-mineral tables, so the first table
becomes the base and cells missing from it are dropped. The first mineral
column is Copper. Every other mineral's treatment group was therefore its
intersection with copper. At 100 km:

| | should be treated | actually treated |
|---|--:|--:|
| Tantalum | 25 | 4 |
| PGMs | 8 | 4 |
| Chromium | 11 | 6 |
| Tin | 12 | 1 |

All seven spatial resolutions were affected. `10_fix_treatment.R` rebuilds the
treatment columns; the originals are untouched.

Two further reporting problems were found alongside it. The `Dir` column in the
mechanism table averaged only the coefficients that reached significance, which
selects on the outcome. And significance was counted against a pointwise 1.96
where the estimator computes a simultaneous critical value near 2.5, so period
counts were inflated. Both are gone; tables now report the dynamic aggregate and
the effect from year ten, with standard errors.

## What holds

**H3 and H4, chromium.** Conflict events fall and battle deaths rise at all seven
scales, with no pre-treatment violations on battle deaths anywhere. The
decoupling argument is intact and better supported than the previous draft
claimed. State-initiated fatalities rise (2.68, SE 1.23 from year ten) and
civilian fatalities rise (0.85, SE 0.43). Formal armed groups are absent from
every treated chromium cell at every resolution, which needs no estimation at
all and is the single most robust fact in the paper.

**H2, PGMs.** Conflict events fall, negative at every scale where estimable.

**H1, tantalum.** Conflict events fall, emerging after year five.

## What changed

**H2 in the old numbering is gone.** Tantalum battle deaths do not fall at any
scale and rise significantly at 150 km. A prediction of reduced lethality under
international governance is contradicted, not merely unconfirmed, so the tier now
carries an events-only prediction. Former H3 to H5 are renumbered H2 to H4.

**The tantalum mechanism reverses.** The old draft reported universal
pacification, with state and civilian violence declining. On corrected data
those outcomes flip sign, and what appears instead is formal armed groups
withdrawing, as initiators (-0.09, SE 0.03) and as targets (-0.19, SE 0.07),
while fatal violence against civilians **rises** (1.57, SE 0.81). The bug had
zeroed out the formal-group outcomes entirely, so these results were invisible.
The story is armed group exclusion without civilian protection, which is a
different and arguably more interesting claim than the one it replaces.

**PGM actor results weaken.** The "12 significant post-treatment periods" finding
does not survive. Formal groups as targets does.

## What to watch

- Chromium conflict events carry eight significant pre-treatment coefficients at
  100 km. They clean up entirely by 300 km, and the text says so, but the
  governance-gap result rests on the weakest identification in the paper.
- Effects appear only after roughly year five, so the estimates lean on the
  earliest discovery cohorts, which have the longest follow-up.
- Chromium and PGMs are both concentrated in South Africa (9 of 13 and 54 of 82
  sites), so that tier contrast is partly a within-country comparison.

## Also done

All 40 comments from the July draft are addressed. The data section now answers
the inclusion-criterion question, the map and framework figure were rebuilt (the
old ones still showed gallium and germanium as the governance-gap tier), figures
3 to 5 are merged into one, the production-onset section is cut, and a post-2010
robustness check is added. Wording throughout is as it was written in the July
draft except where the corrected numbers required a change.
