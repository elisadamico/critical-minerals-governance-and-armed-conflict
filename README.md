# Critical Minerals, Governance and Armed Conflict

## Documents

- **`main_mechanisms.tex`** — the current paper. This is the Overleaf main document.
- **`main_prerevision.tex`** — a frozen copy of the paper as it stood before the
  August 2026 reanalysis, kept for comparison. It reads its tables and figures
  from `prerevision/`, so it compiles on its own and shows the old numbers next
  to the old text. It is a reference point, not a working file.
- **`MEMO.md`** — what changed in the reanalysis and why.

## Directories

| path | contents |
|---|---|
| `latex/` | tables used by `main_mechanisms.tex`, generated from R |
| `plots/` | figures used by `main_mechanisms.tex` |
| `prerevision/` | frozen tables and figures for `main_prerevision.tex` |
| `archive/` | superseded and unused outputs, kept in case they are wanted again |
| `other/` | earlier drafts and slide sources |
| `bib.bib` | bibliography |

Analysis code is not in this repository. It lives alongside it in `REM/`, where
scripts `09` through `21` produce everything in `latex/` and `plots/`.
