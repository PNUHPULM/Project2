# Protocol — Airway-derived liquid biopsy for molecular profiling in NSCLC: a diagnostic test accuracy systematic review and meta-analysis

| Field | Value |
|---|---|
| Version | v0.1 (draft — pre-registration) |
| Date | 2026-08-26 |
| Review type | Diagnostic test accuracy (DTA) |
| Risk-of-bias tool | QUADAS-3 |
| Reporting guideline | PRISMA-DTA (+ PRISMA 2020 for Abstracts; PRISMA-S for the search) |
| Registration | PROSPERO — not yet submitted (see `7_Submission/PROSPERO_registration.md`) |
| Status | Protocol drafting; no searching has begun |

> **Citation status.** All clinical-background citations were resolved on 2026-08-26 against
> PubMed via the PubMed MCP server, and each carries a PMID and DOI verified at that time. No
> citation in this file comes from memory. Bibliographic records are logged in
> `1_Search/citation_verification.md`.

---

## 1. Background and rationale

Comprehensive genomic profiling is required to select targeted therapy in advanced non-small
cell lung cancer (NSCLC), but the two standard specimen types each fail in a predictable way.
Tumour tissue is limited by procedural invasiveness and by spatial heterogeneity, and a
non-diagnostic or quantity-insufficient sample forces a re-biopsy. Plasma cell-free DNA avoids
the procedure but has a substantial false-negative rate, particularly in intrathoracic-only
disease and in low-shedding tumours. In a meta-analysis of 21 studies and 1,639 patients, plasma
ctDNA detected *EGFR* T790M with a pooled sensitivity of only 0.67 (95% CI 0.64-0.70) against a
tissue reference (Passiglia et al., *Sci Rep* 2018;8:13379, PMID:30190486,
doi:10.1038/s41598-018-30780-4), and a separate synthesis put pooled sensitivity for cfDNA
mutation detection at 0.628 (95% CI 0.244-0.919) (Chen et al., *Biomark Med* 2019;14:587-597,
PMID:31845833, doi:10.2217/bmm-2018-0093).

Airway-derived specimens obtained at bronchoscopy — bronchial washing fluid (BWF),
bronchoalveolar lavage fluid (BALF), and fluid collected by a targeted washing technique
delivered through an ultrathin bronchoscope navigated to the lesion — offer a third
compartment. Tumour-derived cell-free DNA is released directly into the airway lumen adjacent
to the tumour, so the specimen is anatomically proximal to the lesion while remaining a fluid
("liquid biopsy") specimen that requires no additional tissue.

Primary studies of this compartment have accumulated rapidly and report detection performance
that is at least comparable to tissue and consistently superior to paired plasma. Reported
figures include a targeted-washing series in which EGFR T790M was detected in 29.3% of
washing-fluid samples versus 22.0% of tissue and 9.8% of plasma samples (Kim et al., *Cancer
Res Treat* 2026;58(1):107-114, PMID:40017263, doi:10.4143/crt.2024.1128), and a prospective NGS
series in which druggable mutations were detected in 65% of BWF samples versus 47% of plasma and
48% of tissue, with 94% BWF-tissue concordance (Kim et al., *JCO Precis Oncol* 2025,
PMID:40749152, doi:10.1200/PO-25-00299). The same direction of effect is reported outside this
group: BAL cfDNA profiled by CAPP-Seq yielded more tumour-derived variants than paired plasma at
every stage (Nair et al., *Cancer Res* 2022;82:2838-2847, PMID:35748739,
doi:10.1158/0008-5472.CAN-22-0554), and *EGFR* mutations were detected in 80% of bronchial
washing supernatants by ddPCR — including in cases where no tumour cells were found by biopsy or
cytology (Murata et al., *Jpn J Clin Oncol* 2024;54:681-688, PMID:38476004,
doi:10.1093/jjco/hyae021).

**No systematic review or diagnostic test accuracy meta-analysis of this specimen class has
been published.** By contrast, the adequacy of EBUS-TBNA specimens for molecular analysis has
been synthesised twice — 33 studies and 2,698 patients giving a pooled *EGFR*-sufficiency of
94.5% (Labarca et al., *Ann Am Thorac Soc* 2018;15:1205-1216, PMID:30011388,
doi:10.1513/AnnalsATS.201801-045OC), and 21 studies and 1,175 patients giving a pooled NGS
adequacy of 86.5% (Zhao et al., *Lung Cancer* 2022;166:17-26, PMID:35151114,
doi:10.1016/j.lungcan.2022.01.018) — and plasma cfDNA genotyping has been synthesised
repeatedly (Passiglia 2018; Chen 2019, both above; Yu et al., *Cell Mol Biol* 2023;69(8):89-95,
PMID:37715416, doi:10.14715/cmb/2023.69.8.14). The evidence for the airway compartment sits in a
state where individual series are persuasive but the pooled operating characteristics — and
the extent to which they depend on collection technique, detection platform, and lesion
factors — are unknown. That is the gap this review addresses.

### 1.1 Objectives

1. To estimate the pooled sensitivity and specificity of airway-derived cell-free DNA for
   detecting *EGFR* mutations in patients with NSCLC, against tissue-based genotyping as the
   reference standard.
2. To estimate the same for *any actionable driver alteration* (secondary synthesis question).
3. To compare, within studies that sampled both compartments from the same patients, the
   sensitivity of airway-derived cfDNA against paired plasma cfDNA.
4. To identify sources of heterogeneity — collection technique, detection platform, lesion
   size, bronchus sign, disease stage, and treatment-line context.

---

## 2. Review question (PIRD)

| Element | Specification |
|---|---|
| **P** — Population | Adults (≥18 y) with cytologically or histologically confirmed NSCLC, or with a lung lesion under investigation for NSCLC, undergoing bronchoscopy. Both treatment-naive and previously treated (including post-TKI progression) patients are eligible. |
| **I** — Index test | Cell-free DNA extracted from the **supernatant** of an airway-derived fluid specimen — bronchial washing fluid, bronchoalveolar lavage fluid, or targeted/lesion-directed washing fluid — analysed by any validated genotyping platform (allele-specific or digital PCR, PNA-clamping, targeted NGS, or comparable). |
| **R** — Reference standard | Genotyping of tumour tissue or a cytology cell-block obtained from the same patient by any route (bronchoscopic, percutaneous, surgical, or metastatic-site biopsy), analysed by a validated platform. |
| **D** — Target condition | **Primary:** presence of an *EGFR* mutation. **Secondary:** presence of any actionable driver alteration (as defined by the primary study, recorded verbatim). |

**Comparator (not part of PIRD; a pre-specified secondary comparison).** Plasma cell-free DNA
genotyping performed on a sample drawn from the same patient in the same episode of care.

---

## 3. QUADAS-3 Phase 1 — synthesis questions

QUADAS-3 phases 1 and 2 are review-level and are fixed here, before any study is seen. Every
later risk-of-bias and applicability judgement is made against the ideal trial defined in §4.

| # | Synthesis question | Priority |
|---|---|---|
| SQ1 | In adults with NSCLC undergoing bronchoscopy, what is the accuracy of *EGFR* genotyping on airway-derived cell-free DNA, compared with tissue genotyping, for identifying patients whose tumour carries an *EGFR* mutation? | Primary |
| SQ2 | In the same population, what is the accuracy of airway-derived cell-free DNA for identifying patients whose tumour carries any actionable driver alteration? | Secondary |
| SQ3 | In patients from whom airway fluid and plasma were sampled in the same episode, how does the sensitivity of airway-derived cfDNA compare with that of paired plasma cfDNA, against the same tissue reference standard? | Secondary (paired, within-study) |

SQ3 is a comparative accuracy question and will be assessed with **QUADAS-C** layered on
QUADAS-3, restricted to studies contributing both compartments.

---

## 4. QUADAS-3 Phase 2 — the ideal test accuracy trial

Defined once per synthesis question, in advance.

### 4.1 Ideal trial for SQ1 (and, with the target condition substituted, SQ2)

| Element | Specification |
|---|---|
| **Objective** | Estimate the sensitivity and specificity of airway-derived cfDNA genotyping for the presence of an *EGFR* mutation in the tumour. |
| **Participants** | A consecutive or random sample of adults presenting for bronchoscopic evaluation of a lung lesion suspected or confirmed to be NSCLC, enrolled prospectively under a **single-gate** design — that is, recruited on presentation, before either test result is known, and not sampled separately by known mutation status. |
| **Index test** | Airway fluid collected by a pre-specified, reproducibly described technique; supernatant separated and cfDNA extracted per a stated protocol; genotyped on a platform with a stated limit of detection and a pre-specified variant-calling threshold; interpreted **blind to the tissue result**. |
| **Target condition** | An *EGFR* mutation present in the tumour, as determined by genotyping of adequate tumour tissue from the same patient on a validated platform, interpreted blind to the airway result. Applied to **every** enrolled participant regardless of the index-test result, and by the **same** method in every participant. |
| **Analysis** | All enrolled participants accounted for. A single 2x2 table at the patient level. Unevaluable index tests reported and handled in an intention-to-diagnose analysis, not silently excluded. Sensitivity and specificity computed with the tissue result as the reference in every cell. |

### 4.2 Ideal trial for SQ3 (comparative)

As §4.1, with both index tests (airway cfDNA and plasma cfDNA) performed on **every**
participant in the same episode of care, each interpreted blind to the other and to the
reference standard, and both compared against the same tissue reference standard within the
same participants. Paired 2x2 data (or a paired discordance table) reported.

### 4.3 Review-specific guidance for the signalling questions

Written in advance, to be published as a web appendix. Full 20-question guidance lives in
`0_Protocol/quadas3_guidance.md`; the judgements most likely to differentiate studies in this
review are fixed here:

| SQ | Review-specific rule |
|---|---|
| **1.1** (single-gate) | A study that enrolled a fixed number of known *EGFR*-mutant and known wild-type patients is **two-gate** → high risk. Enrolment of consecutive bronchoscopy patients is single-gate → low risk. |
| **1.4** (representative) | Concern if the cohort is restricted to lesions with a positive bronchus sign, to central lesions, or to a single stage stratum, without this being the stated intended-use population. |
| **2.2** (index blind) | Airway cfDNA genotyping performed **after** the tissue result was known and available to the laboratory is high risk. Batched retrospective testing of banked supernatant is low risk if the tissue result was not supplied to the operator. |
| **2.4** (threshold) | The variant-allele-frequency call threshold must be stated and pre-specified. A threshold chosen post hoc to optimise agreement with tissue is high risk. |
| **3.1** (adequate reference) | Tissue genotyping on a platform whose panel does not cover the alteration being called in the airway sample does not adequately identify the target condition. Panel breadth must be recorded per study and compared across compartments. |
| **3.2** (assessed in all) | Studies in which tissue genotyping was attempted only where the airway result was positive, or only where tissue was "sufficient", carry **partial verification bias** → high risk. This is expected to be the dominant bias in this literature and is a pre-specified sensitivity analysis. |
| **3.4** (no incorporation) | If the airway result contributed to the composite that defined the reference standard — for example, a "true positive by any method" definition — the reference standard **incorporates** the index test → high risk. Studies using an any-method composite reference are a pre-specified sensitivity-analysis exclusion. |
| **4.3** (unit of analysis) | The unit must be the **patient**. A study pooling multiple specimens or multiple alterations per patient as independent observations does not match the ideal trial. |
| **4.4** (estimates) | Detection *rate* (proportion positive) is **not** sensitivity. A study reporting only detection rates without a tissue-verified 2x2 cannot contribute to the DTA pool; see §6.2. |

---

## 5. Eligibility criteria

### 5.1 Inclusion

- **Design:** prospective or retrospective cohort or cross-sectional studies reporting
  diagnostic accuracy; single-arm and comparative designs both eligible.
- **Population:** as §2. Minimum **10** patients contributing index and reference results.
- **Index test:** cfDNA from airway fluid **supernatant** (BWF, BALF, or targeted washing
  fluid), any genotyping platform.
- **Reference standard:** tissue or cell-block genotyping in the same patients.
- **Outcome:** sufficient data to reconstruct a patient-level 2x2 table (TP/FP/FN/TN), either
  reported directly or derivable from reported sensitivity/specificity with denominators, or
  from a concordance table.
- **Language:** English. Non-English records with an English abstract are screened and their
  exclusion at full text is recorded as a language exclusion, so the restriction is auditable.
- **Date:** 2010-01-01 to the search date. Justification: pre-2010 series predate routine
  EGFR-directed genotyping and the sensitive allele-specific platforms on which this specimen
  class depends.

### 5.2 Exclusion (with justification)

| Code | Criterion | Justification |
|---|---|---|
| E1 | Not NSCLC / not a lung-lesion population | Outside the intended-use population |
| E2 | Index test is not airway-fluid **supernatant** cfDNA — e.g. cell pellet/sediment, cytology smear, tissue, sputum, exhaled breath condensate, pleural fluid | Pre-specified index-test boundary (§2); sediment is a cellular specimen, not a liquid-biopsy compartment |
| E3 | No tissue-based reference standard in the same patients | Accuracy cannot be estimated |
| E4 | Ineligible publication type — review, editorial, case report, conference abstract without extractable 2x2 | Insufficient data and no assessable methods |
| E5 | Non-human / cell-line / methodological-validation-only study | Not a clinical accuracy study |
| E6 | Fewer than 10 evaluable patients | Unstable estimates; pre-specified floor |
| E7 | Duplicate or overlapping cohort | Double counting (see §7.3) |

Conference abstracts are **excluded** from the pool but retained in a grey-literature list and
used only to assess the possibility of unpublished data (§9.4).

---

## 6. Outcomes

### 6.1 Primary outcome

Pooled sensitivity and specificity (with 95% CIs) of airway-derived cfDNA for *EGFR* mutation
detection, against tissue genotyping, summarised as a bivariate estimate and an SROC curve
with confidence and prediction regions.

### 6.2 Secondary outcomes

1. Pooled sensitivity/specificity for any actionable driver alteration (SQ2).
2. Paired within-study comparison of airway versus plasma cfDNA sensitivity (SQ3), expressed as
   a ratio of sensitivities / difference in sensitivity with a paired variance.
3. Pooled **assay success rate** (proportion of collected airway specimens yielding an
   interpretable genotyping result) — a single-arm proportion synthesis, reported separately
   and never merged into the DTA pool.
4. Pooled concordance (overall percent agreement and Cohen's κ) between airway and tissue.
5. Adverse events attributable to airway-fluid collection.

> **Outcome 3 is a proportion, not an accuracy estimate.** It is registered as a distinct
> synthesis with its own model (`metaprop`) and its own certainty rating. Detection rate is
> never reported as sensitivity anywhere in this review (QUADAS-3 4.4, §4.3).

---

## 7. Search and study selection

### 7.1 Databases

PubMed/MEDLINE, Embase, and Cochrane CENTRAL (minimum three), plus Scopus and Web of Science
Core Collection. Trial registries: ClinicalTrials.gov and WHO ICTRP, for unpublished or
in-progress studies. Backward and forward citation chasing on every included study and on the
two prior reviews of adjacent specimen classes.

Searches will be executed via `/search-lit` and reported per **PRISMA-S** (Rethlefsen et al.,
*Syst Rev* 2021, PMID:33499930), one section per database with the exact string, interface,
date run, and result count.

### 7.2 Draft search blocks

To be peer-reviewed against **PRESS** before execution and validated against a seed set of
known-eligible records (§7.2.1).

```
# Block A — Population
"lung neoplasms"[MeSH] OR "carcinoma, non-small-cell lung"[MeSH]
OR "lung cancer"[tiab] OR "NSCLC"[tiab] OR "pulmonary neoplasm*"[tiab]
OR "lung adenocarcinoma"[tiab]

# Block B — Index specimen
"bronchoalveolar lavage fluid"[MeSH] OR "bronchoalveolar lavage"[tiab]
OR "BALF"[tiab] OR "bronchial washing*"[tiab] OR "bronchial lavage"[tiab]
OR "bronchial wash"[tiab] OR "BWF"[tiab] OR "airway lavage"[tiab]
OR "targeted washing"[tiab] OR "lesion-directed washing"[tiab]
OR (("bronchoscop*"[tiab]) AND ("wash*"[tiab] OR "lavage"[tiab]))

# Block C — Analyte / test
"cell-free nucleic acids"[MeSH] OR "circulating tumor DNA"[MeSH]
OR "cell-free DNA"[tiab] OR "cfDNA"[tiab] OR "ctDNA"[tiab]
OR "liquid biopsy"[tiab] OR "supernatant"[tiab]
OR "high-throughput nucleotide sequencing"[MeSH]
OR "next-generation sequencing"[tiab] OR "NGS"[tiab]
OR "digital PCR"[tiab] OR "ddPCR"[tiab] OR "PNA clamping"[tiab]

# Block D — Target condition
"ErbB Receptors"[MeSH] OR "EGFR"[tiab] OR "epidermal growth factor receptor"[tiab]
OR "T790M"[tiab] OR "driver mutation*"[tiab] OR "actionable mutation*"[tiab]
OR "genomic profiling"[tiab] OR "molecular profiling"[tiab] OR "genotyping"[tiab]

# Combination
A AND B AND (C OR D)
```

No methodological/DTA filter will be applied: DTA filters are known to lose eligible records,
and the topic-specific blocks are already narrow.

#### 7.2.1 Seed-set validation (gate executed 2026-08-26 — PASS)

The strategy must retrieve **all** of the following known-eligible records before it is run at
scale. Failure to retrieve any seed sends the strategy back for revision, and the revision is
logged.

Run against PubMed on 2026-08-26. Sub-query labels (QA/QB/QC) are defined in
`1_Search/pubmed_strategy.md`; QA = analyte block anchored on a cancer term, QB = platform block
anchored on *EGFR*/mutation, QC = extracellular-vesicle block.

| Seed | PMID | Retrieved by | Result |
|---|---|---|---|
| Kim 2026 — targeted washing technique, *EGFR* T790M | 40017263 | QB | PASS |
| Kim 2025 — BWF ctDNA NGS vs plasma vs tissue | 40749152 | QA | PASS |
| Murata 2024 — BWF supernatant cfDNA, ddPCR | 38476004 | QA, QB | PASS |
| Nair 2022 — BAL cfDNA, CAPP-Seq | 35748739 | QA | PASS |
| Ryu 2019 — BW supernatant, ultra-deep NGS | 31036768 | QA | PASS |
| Hur 2018 — BALF extracellular-vesicle DNA, *EGFR* | 29374476 | QA, QB, QC | PASS |

**The gate passes only on the union — never on any single sub-query.** QB is the only block that
retrieves the targeted-washing seed (40017263); QA is the only block that retrieves Nair and Ryu.
Any future amendment that drops a sub-block must re-run this gate before execution.

### 7.3 Screening

Per skill Phase 3 (rounds R1-R4), two independent reviewers throughout, Cohen's κ reported at
title/abstract and at full text, disagreements to consensus or a third reviewer.

Full-text exclusion codes: F1 no extractable 2x2; F2 no paired-compartment data (SQ3 only);
F3 target population not separable; F4 n<10 evaluable; F5 full text unavailable.

**Overlapping cohorts.** The literature is concentrated in a few high-volume bronchoscopy
centres, so cohort overlap is expected rather than exceptional. `cohort_overlap_check.py` is
run at Phase 4c; HIGH-confidence pairs are resolved by retaining the report with the larger
evaluable n (or the one matching the primary target condition), with the excluded partner
listed and a sensitivity analysis run the other way.

**Reviewer independence.** Members of the review team are co-authors on candidate studies. Any
record authored by a review-team member is screened, extracted, and risk-of-bias assessed by
**two reviewers who are not authors of that record**, and this is stated in Methods.

---

## 8. Data extraction

Dual independent extraction into `templates/extraction_form_v2.md` (source page reference and
verbatim quote per numeric cell). Fields, beyond the standard bibliographic set:

- **Design:** prospective/retrospective; single- vs two-gate; consecutive enrolment; country;
  enrolment period; single vs multicentre.
- **Population:** n enrolled / n evaluable; age; stage distribution; histology; treatment line
  (naive vs post-TKI); lesion size; bronchus sign; central vs peripheral.
- **Index test:** fluid type (BWF / BALF / targeted washing); instilled volume; bronchoscope
  type and calibre; navigation (VBN, RP-EBUS, fluoroscopy, none); whether the scope was wedged
  or advanced to the lesion; supernatant separation protocol; cfDNA extraction kit; platform;
  panel/gene coverage; VAF calling threshold; blinding.
- **Reference standard:** tissue source and route; platform; panel breadth; blinding; interval
  between index and reference; whether applied to all participants.
- **Comparator (where present):** plasma volume, tube type, processing interval, platform.
- **Outcomes:** 2x2 cells at patient level for each target condition; assay success rate;
  concordance/κ; adverse events; paired discordance table for SQ3.

Where a study reports sensitivity/specificity with denominators but not the cells, the cells
are back-calculated and the reconstruction is recorded; `dta_extraction_qc.py` then re-derives
sensitivity and specificity from the cells and flags any disagreement beyond 0.02.

**Missing data.** Corresponding authors are contacted twice, 14 days apart, for missing 2x2
cells. Studies that remain unreconstructable after contact are listed in the excluded-at-
full-text table with reason F1 and cited individually (PRISMA item 16b).

---

## 9. Synthesis

### 9.1 Model

Bivariate random-effects model (Reitsma et al., *J Clin Epidemiol* 2005;58:982-990) via
`mada::reitsma()` in R, with the HSROC parameterisation (Rutter & Gatsonis, *Stat Med*
2001;20:2865-2884) reported alongside. The model is chosen **because sensitivity and
specificity are correlated within studies and a common true accuracy across these
populations is not plausible** — not because a heterogeneity statistic exceeded a threshold.

Outputs: pooled sensitivity and specificity with 95% CIs; SROC curve with 95% confidence and
prediction regions; paired forest plots.

**If k < 4 for a given synthesis question**, the bivariate model is not fitted. The fallback,
pre-specified: univariate random-effects pooling of sensitivity and of specificity separately
(logit transform, REML), reported with an explicit statement that the correlation structure is
unmodelled, plus a narrative synthesis. Below k=4 no subgroup analysis or meta-regression is
performed.

### 9.2 Assay success rate (Outcome 3)

`meta::metaprop()` with logit transform and REML; Clopper-Pearson CIs for individual studies.
Not pooled with any accuracy estimate.

### 9.3 Comparative synthesis (SQ3)

Restricted to studies reporting both compartments in the same patients. Paired analysis on the
within-study log ratio of sensitivities with its paired variance where a discordance table is
available; where only marginal sensitivities are reported, the pair is analysed with an assumed
correlation and the assumption is varied (0.3 / 0.5 / 0.7) as a sensitivity analysis. Assessed
with QUADAS-C.

### 9.4 Heterogeneity, threshold effect, and reporting bias

- Between-study heterogeneity: prediction region on the SROC plot as the primary
  representation; τ² reported. I² is **not** used as the primary heterogeneity statistic for
  the bivariate model.
- Threshold effect: Spearman correlation between sensitivity and false-positive rate, plus
  visual inspection of the SROC shoulder.
- Reporting bias: **Deeks' funnel plot asymmetry test** (not a standard funnel plot), run only
  if k ≥ 10, with an explicit statement of low power otherwise.
- Registries and the grey-literature abstract list are used to identify completed-but-
  unpublished studies.

### 9.5 Subgroup analyses (pre-specified; only if k ≥ 10 per stratum)

1. **Fluid type / collection technique:** targeted (lesion-directed) washing vs conventional
   bronchial washing vs BALF. *Primary subgroup — this is the review's main mechanistic
   hypothesis: proximity of collection to the lesion drives yield.*
2. **Detection platform:** targeted NGS vs digital/allele-specific PCR.
3. **Treatment context:** treatment-naive (activating mutation) vs post-TKI progression
   (resistance mutation, e.g. T790M).
4. **Disease stage:** early/locally advanced vs advanced/metastatic.
5. **Lesion factors:** bronchus sign present vs absent; central vs peripheral; size threshold
   ≤30 mm vs >30 mm.
6. **Reference-standard route:** bronchoscopic vs non-bronchoscopic tissue.

Meta-regression on the same covariates, only if k ≥ 10 overall, with the number of covariates
capped at k/10.

### 9.6 Sensitivity analyses

1. Excluding studies at high risk of bias on QUADAS-3 domain 3 (target condition).
2. Excluding studies with partial verification (SQ 3.2 high risk).
3. Excluding studies using an any-method composite reference standard (SQ 3.4 high risk).
4. Excluding retrospective studies.
5. Excluding one of each HIGH-confidence overlapping-cohort pair.
6. Excluding studies authored by review-team members.
7. Varying the assumed within-study correlation in SQ3 (§9.3).

Every sensitivity analysis is **recomputed on the modified dataset**, never transcribed.

---

## 10. Risk of bias and certainty

**QUADAS-3**, phases 3-6, per accuracy estimate, by two independent assessors with consensus
or a third assessor; review-specific guidance fixed at §4.3 and `quadas3_guidance.md`.
**QUADAS-C** additionally for SQ3. Per-study, per-domain judgements are reported study-by-study
(traffic-light plot), not only as pooled proportions (PRISMA item 18).

**GRADE-DTA**, rated **per outcome**, not once for the review: risk of bias, indirectness,
inconsistency, imprecision, publication bias. Where k < 4 the domains are assessed narratively
and the limitation stated. Summary of Findings table carries one row per outcome with the
pooled estimate, its precision, and the certainty rating with the reason for each downgrade.

---

## 11. Data availability

The extraction form, the locked extraction dataset, the QUADAS-3 per-study judgements, and all
analysis code will be deposited in this repository and archived with a DOI on acceptance
(PRISMA item 27). Full-text PDFs are not redistributable and are excluded by `.gitignore`.

---

## 12. Amendments

Any change after registration is recorded here with date and rationale, and filed as a formal
PROSPERO amendment.

| Date | Section | Change | Rationale |
|---|---|---|---|
| — | — | — | — |

---

## 13. Open items before registration

| # | Item | Status | Owner |
|---|---|---|---|
| 1 | Resolve every `[CITE]` against PubMed (none from memory) | **Done** 2026-08-26 | — |
| 2 | Complete the seed set in §7.2.1 and run the retrieval gate | **Done** — PASS | — |
| 3 | Execute PubMed + Embase | Run sheet ready (`1_Search/RUN_SHEET.md`); awaiting exports. CENTRAL / Scopus / WoS still open | — |
| 4 | PRESS peer review of the search strategy | Open | — |
| 5 | Confirm review team, roles, and the reviewer-independence assignment (§7.3) | Open | — |
| 6 | Confirm funding and COI statements | Open | — |
| 7 | Write the full 20-question `quadas3_guidance.md` web appendix | **Done** — `0_Protocol/quadas3_guidance.md` | — |
| 8 | Submit to PROSPERO and record the CRD ID (`^CRD42\d{9}$`) | Open | — |
