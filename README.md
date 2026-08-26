# Airway-derived liquid biopsy for molecular profiling in NSCLC

A diagnostic test accuracy (DTA) systematic review and meta-analysis.

**Question.** In patients with NSCLC undergoing bronchoscopy, how accurately does cell-free
DNA from airway fluid supernatant (bronchial washing, BAL, or targeted washing fluid) detect
*EGFR* mutations — and actionable driver alterations generally — against tissue genotyping?
And how does it compare with paired plasma cfDNA?

No systematic review or DTA meta-analysis of this specimen class has been published.

## Status

| Phase | State |
|---|---|
| 1 — Protocol | Draft ([`0_Protocol/protocol.md`](0_Protocol/protocol.md)) |
| 1 — PROSPERO registration | Not yet submitted |
| 2 — Search | Not started |
| 3-10 | Not started |

## Layout

| Directory | Contents |
|---|---|
| `0_Protocol/` | Protocol, QUADAS-3 review-specific guidance |
| `1_Search/` | Per-database strategies and results (PRISMA-S) |
| `2_Screening/` | Screening rounds, consensus, pool lock |
| `3_Extraction/` | Extraction forms, locked dataset, QC |
| `4_RoB/` | QUADAS-3 / QUADAS-C judgements |
| `5_Analysis/` | R analysis scripts and output logs |
| `6_Tables/` | Manuscript tables |
| `7_Submission/` | PROSPERO document, manuscript, supplement |

Reporting follows PRISMA-DTA, PRISMA 2020 for Abstracts, and PRISMA-S.
Risk of bias uses QUADAS-3 (QUADAS-C for the comparative question).

Toolchain and its pinned version: [`docs/skills-setup.md`](docs/skills-setup.md).
