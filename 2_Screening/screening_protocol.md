# Screening procedure

Operational companion to protocol §7.3. Four rounds, two independent reviewers throughout,
Cohen's κ reported at title/abstract and at full text.

## Who screens, and what my role is

This matters for Methods and must be settled before round 1, not written up afterwards.

| Role | Who |
|---|---|
| Reviewer 1 (human) | *to be named* |
| Reviewer 2 (human) | *to be named* |
| Third reviewer / adjudicator | *to be named* |
| AI second-pass tool | Claude (Opus 5), used as a **documented screening aid** |

**My suggestions are not decisions.** Every record I mark is confirmed or overturned by a named
human reviewer before it counts, and the Methods section must say so explicitly. An AI pass does
not substitute for either independent human reviewer, and κ is computed between the two **human**
reviewers, not between a human and me.

If that is not what you want, say so and I will restrict myself to building the sheets and
computing the reconciliation, with no screening marks at all.

### Reviewer independence for review-team papers

Protocol §7.3: records authored by review-team members — currently PMIDs **40017263** and
**40749152**, and any further hits from this group — are screened, extracted and risk-of-bias
assessed by **two reviewers who are not authors of that record**. Flag these rows on sight; the
column `team_authored` exists for it. State the arrangement in Methods.

## Rounds

| Round | What | Reviewers | Output |
|---|---|---|---|
| R1 | Title/abstract, first pass | 1 human | `round1_<date>.tsv` |
| R2 | Title/abstract, independent second pass | 2nd human (+ AI aid, documented) | `round2_<date>.tsv`, κ |
| R3 | Adjudication of every MAYBE and a confirmation sweep of INCLUDEs | 1st human | `round3_adjudication.tsv` |
| R4 | Full text | 2 humans | `fulltext_screening.tsv`, κ |

MAYBE at R2 means **disagreement, or either reviewer flagged uncertainty** — not "unsure, decide
later". R3 resolves every one.

## Exclusion codes

Title/abstract (from protocol §5.2 — these are the *registered* codes; do not invent new ones
mid-screening, and do not renumber):

| Code | Meaning |
|---|---|
| E1 | Not NSCLC / not a lung-lesion population |
| E2 | Index test is not airway-fluid **supernatant** cfDNA (cell pellet, cytology smear, tissue, sputum, exhaled breath condensate, pleural fluid) |
| E3 | No tissue-based reference standard in the same patients |
| E4 | Ineligible publication type (review, editorial, case report, conference abstract without extractable 2x2) |
| E5 | Non-human / cell-line / methodological-validation only |
| E6 | Fewer than 10 evaluable patients |
| E7 | Duplicate or overlapping cohort |

Full text:

| Code | Meaning |
|---|---|
| F1 | No extractable patient-level 2x2 (**includes: detection rate reported without a tissue-verified 2x2**) |
| F2 | No paired-compartment data (SQ3 only) |
| F3 | Target population not separable |
| F4 | Fewer than 10 evaluable patients |
| F5 | Full text unavailable |

A validity gate runs before write-up: `check_exclusion_code_validity.py` checks every applied code
against the registered eligibility criteria and fails on a code that excludes a design the protocol
includes.

## Screening decision aids

Judgement calls this review will hit repeatedly. Decide them the same way every time.

| Situation | Decision |
|---|---|
| Supernatant vs cell pellet not distinguishable from the abstract | **MAYBE** → full text. Do not exclude at title/abstract on E2 unless the abstract says pellet/sediment/cytology explicitly. |
| Sputum, exhaled breath condensate, pleural fluid | **E2.** Outside the registered index-test boundary. |
| Airway fluid used for *diagnosis of malignancy*, no genotyping | **E1/E2** — the target condition is a driver alteration, not cancer per se. Record which. |
| Detection rate only, no tissue comparison | Passes title/abstract; excluded at full text as **F1**. It may still contribute to the assay-success-rate synthesis (§6.2(3)) — mark `success_rate_only = Y` so it is not lost. |
| Conference abstract | **E4**, but keep in the grey-literature list (§9.4) for the unpublished-data assessment. |
| Same group, overlapping period | Do **not** resolve at title/abstract. Include both, flag `overlap_suspect`, and resolve at Phase 4c with `cohort_overlap_check.py`. |
| Non-English with English abstract | Screen it. If excluded at full text for language, record it as a language exclusion so the restriction is auditable. |

## `round1.tsv` schema

Tab-separated. One row per deduplicated record.

```
uid          stable review-local ID (PM00001…), assigned at dedup, never reused
pmid
doi
source       pubmed | embase | both
year
journal
first_author
title
abstract
r1_decision  INCLUDE | EXCLUDE | MAYBE
r1_code      E1–E7, blank if INCLUDE/MAYBE
r1_note
team_authored        Y/N — review-team authorship (independence rule)
overlap_suspect      Y/N
success_rate_only    Y/N
```

R2 adds `r2_decision`, `r2_code`, `r2_note`; R3 adds `round3_decision`, `round3_reason` (required
only when overturning R2).

## Deduplication

DOI first, then PMID, then normalised title + year. Records merged across databases get
`source = both`. Raw per-database counts are preserved for the PRISMA flow **before** dedup — the
flow needs identified, duplicates removed, and screened as separate numbers.

## Gates before write-up

1. `screening_reconcile.py` — reconciles counts from raw ID sets, never from prose. Every "N → M"
   transition needs the added/removed IDs listed. A record included at screening but absent from
   the consensus artifact is a P0.
2. `FINAL_POOL_LOCK.yaml` — freeze the pool with a SHA-256 over the sorted UID list before any
   extraction. `k included` is read from the lock, never re-derived from the extraction sheet.
3. `check_exclusion_code_validity.py --strict`.

## Status

Waiting on the PubMed and Embase exports (`1_Search/RUN_SHEET.md`). Nothing has been screened.
