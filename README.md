# Critical Minerals, Governance and Armed Conflict: Evidence from Africa

Elisa D'Amico (University College Dublin) and Päivi Lujala (University of Oulu).

This repository is a GitHub mirror of the project's Overleaf source. It tracks
the writing (manuscript, submission files, slides, tables, and figures), not
the underlying datasets or analysis code, which live outside this repository.

## Abstract

The clean energy transition has sharply increased demand for critical
minerals, many of which are concentrated in regions with weak governance and
histories of resource-related conflict. Africa, which holds substantial
reserves, sits at the center of this challenge. Using geocoded mineral
discovery data and staggered difference-in-differences estimates across
multiple spatial scales (1995-2018), we show that the conflict effects of
mineral discovery depend systematically on the governance regime surrounding
extraction. Three distinct patterns emerge. International due diligence
frameworks reduce conflict frequency and remove organized armed groups, yet
civilian security does not improve and lethality remains unchanged. National
governance produces the strongest pacification effects: both conflict
frequency and battle deaths decline, and violence by state actors and against
civilians decreases. Minerals lacking governance frameworks exhibit a
decoupling pattern in which conflict events fall but battle deaths rise,
driven by increased state lethality and higher civilian fatalities. These
results demonstrate that governance can weaken the link between mineral
wealth and organized armed violence, but they also show that excluding armed
groups is not equivalent to protecting civilians.

Submitted to *Environment and Security* (Sage).

## Data

The analysis combines two sources.

- **Mineral discoveries.** Geocoded exploration and discovery records from the
  S&P Global Market Intelligence database, covering 22 critical minerals
  across Africa, with coverage running to 2018. The paper focuses on three of
  them, chosen to represent distinct governance regimes: tantalum (a 3T
  mineral under international due diligence, e.g. Dodd-Frank Section 1502 and
  ITSCI), platinum group metals (regulated under South Africa's national
  Mineral and Petroleum Resources Development Act), and chromium (a
  governance-gap mineral with no comparable oversight).
- **Conflict events.** The Uppsala Conflict Data Program Georeferenced Event
  Dataset (UCDP-GED v25.1), and, for the actor-level mechanism analysis, the
  UCDP Actor Dataset (v25.1), which classifies each side of a conflict event
  by organizational type (formal military organizations, political
  organizations, identity-based groups, state actors, civilians).

The unit of analysis is a hexagonal grid-year cell covering the African
continent, constructed at seven spatial resolutions (25km-300km diameter) for
robustness; the main analysis uses the 100km resolution. The study period is
1995-2018, with mineral discoveries recorded from 1997 onward.

**This repository does not contain the underlying datasets, derived panels,
or estimation code.** Per the manuscript, replication data and detailed
instructions will be made available upon publication.

## Repository structure

- `main_mechanisms.tex` — current manuscript (anonymized for double-blind
  review; author details live on the separate title page below).
- `latex/` — table and figure includes for the main manuscript.
- `plots/` — figures.
- `submission/` — title page (authors, ORCIDs, acknowledgements, author
  contributions, declarations) and cover letter for the journal submission.
  Kept separate from the manuscript to meet the journal's double-anonymized
  review requirements.
- `deck/` — conference presentation materials (APSA 2026).
- `other/` — earlier or alternate full drafts (including an older title,
  "Minerals, Markets, and Armed Conflict: Critical Minerals in the Modern
  Green Economy").
- `prerevision/`, `archive/` — superseded drafts and analysis versions kept
  for reference.
- `bib.bib` — bibliography.

## Status

In submission to *Environment and Security*. Source of truth for the writing
is the linked Overleaf project; this mirror is updated periodically and may
lag it.
