# QUADAS-3 review-specific guidance (web appendix)

Companion to `0_Protocol/protocol.md`. Written **before any study was screened**, per the QUADAS-3
Explanation & Elaboration requirement that tailoring happen at the protocol stage rather than once
the studies are in view. Defining the rules after seeing the data is not assessment; it is a
judgement fitted to the results.

| Field | Value |
|---|---|
| Review | Airway-derived liquid biopsy for molecular profiling in NSCLC (DTA) |
| Tool | QUADAS-3 v1.2 — 6 phases, 4 domains, 20 signalling questions (4/4/8/4) |
| Additional tool | QUADAS-C (adapted) for synthesis question SQ3 |
| Version | v1.0, 2026-08-26 |
| Assessors | Two independent, per estimate; disagreement to a third |

> **Use the official form.** QUADAS-3 is published in *Annals of Internal Medicine* under no open
> licence. This appendix gives **our review-specific rules for answering** each signalling
> question; it does not reproduce the published wording. Every assessment must be recorded on the
> official `QUADAS-3 1.2.docx` obtained from the QUADAS group
> (https://www.bristol.ac.uk/population-health-sciences/projects/quadas/quadas-3/), and assessors
> must read the E&E report (Davenport et al., *Ann Intern Med* 2026;179(4):e2504943,
> doi:10.7326/ANNALS-25-04943) before first use.

---

## How to use this appendix

**Answers.** Each signalling question takes Y / PY / PN / N / NI. Use **NI** only when the report
gives too little to judge — it is not a middle grade between low and high risk.

**Domain judgement is judgement, not arithmetic.** A "no" or "probably no" *flags potential* for
bias; it does not settle it. Assessors then decide whether the issue plausibly moved the accuracy
estimate for **this** synthesis question. An estimate can be low risk with a "no" recorded. Do not
implement "any No → High".

**Overall (phase 6), per estimate, separately for risk of bias and applicability.** Any domain high
→ overall high. All low → low. Any II and none high → II. **No "moderate" grade** — the QUADAS-3
authors explicitly reject one.

**No question is removed.** Several below can rarely bite given our eligibility criteria (1.1, 3.4).
They stay, and recording that they were considered is the point.

**Every judgement is made against the ideal test accuracy trial** in protocol §4 — not against an
unstated ideal, and not against what is typical in this literature. "Everyone does it this way" is
not a reason to answer yes.

### The four failure modes this appendix is built around

Anticipated before screening, from what this literature looks like:

1. **Partial verification (3.2).** Tissue genotyping attempted only where tissue was adequate, or
   only where the airway result was positive. Expected to be the dominant bias.
2. **Panel-breadth mismatch (3.1).** A single-gene PCR tissue reference against a targeted-NGS
   airway index. Discordance then measures panel coverage, not accuracy.
3. **Detection rate reported as sensitivity (4.4).** Widespread in this field. A tissue-verified
   2x2 is required; a proportion-positive is not an accuracy estimate.
4. **Same-specimen incorporation (3.4).** Where the "tissue" comparator was derived from the cell
   pellet of the same washing that supplied the supernatant index test.

---

# Domain 1 — Participants

*Applicability: does the included population match the ideal trial's — adults presenting for
bronchoscopic evaluation of a lung lesion suspected or confirmed to be NSCLC and requiring
genotyping?*

### 1.1 — Single-gate design

**What it asks here.** Were participants recruited as one group on presentation, rather than
sampled separately according to whether they already carried the target alteration?

| Answer | Rule |
|---|---|
| **Y** | Consecutive or unselected patients enrolled at bronchoscopy, before any genotype was known. |
| **PY** | A single clinical cohort with minor administrative exclusions unrelated to genotype. |
| **PN** | Enrolment restricted to patients already known to have adequate tissue for genotyping — a soft second gate on the reference standard. |
| **N** | A fixed number of known-mutant and known-wild-type patients enrolled (two-gate / diagnostic case-control). Also: post-TKI cohorts assembled by known T790M status. |
| **NI** | Recruitment route not described. |

**Note.** Two-gate designs inflate both sensitivity and specificity by removing diagnostically
ambiguous patients. Our eligibility does not exclude them, so this question will bite. A study
enrolling a mutation-enriched cohort *and* reporting a 2x2 is eligible but answers N here.

### 1.2 — Prospective enrolment

| Answer | Rule |
|---|---|
| **Y** | Airway fluid collected prospectively under a protocol that pre-specified the index test. |
| **PY** | Retrospective analysis of specimens collected under a **pre-existing prospective protocol** that specified supernatant separation and storage — the specimen handling was not chosen after the fact. |
| **PN** | Retrospective use of banked fluid where the storage protocol was not designed for cfDNA. |
| **N** | Specimens assembled retrospectively from residual clinical material, with the analysis plan written afterwards. |
| **NI** | Direction of the study not stated. |

**Note.** Retrospective is not automatically high risk here; what matters is whether pre-analytic
handling (time to centrifugation, storage temperature) was governed by a protocol or by chance.
Where it was not, the bias usually lands on 2.1, not here.

### 1.3 — Consecutive or random sample

| Answer | Rule |
|---|---|
| **Y** | "Consecutive" stated explicitly, with a defined recruitment window. |
| **PY** | All eligible patients over a stated period, with accounted-for exclusions. |
| **PN** | Convenience sampling not obviously related to the target condition. |
| **N** | **Selection on residual specimen volume or on cfDNA yield.** Enrolling only patients whose leftover fluid was sufficient selects for high tumour-DNA shedding and inflates sensitivity. |
| **NI** | Sampling method not described. |

**Note.** Volume/yield-based selection is the review-specific trap in this question and is easy to
miss because it is usually reported as a methods detail rather than as an eligibility criterion.
Read the specimen-handling paragraph, not just the eligibility paragraph.

### 1.4 — Representative of the intended-use population

**Intended use:** patients undergoing bronchoscopy for a lung lesion suspected or confirmed to be
NSCLC in whom genotyping is clinically required — including those in whom tissue is expected to be
scarce, which is the population the test is for.

| Answer | Rule |
|---|---|
| **Y** | Unrestricted bronchoscopy population spanning central and peripheral lesions, and a range of stages. |
| **PY** | A stated restriction that matches a defensible clinical sub-use (e.g. post-TKI progression only), with the restriction reported. |
| **PN** | Restricted to bronchus-sign-positive or endobronchially visible lesions without stating this as the intended use. |
| **N** | Restricted to patients with abundant tissue, or to advanced-stage high-burden disease only, such that the tissue-scarce population the test targets is absent. |
| **NI** | Lesion and stage characteristics not reported. |

**Applicability concern** is recorded separately and is *high* whenever the cohort is confined to
one lesion type, one stage stratum, or one treatment line, regardless of the risk-of-bias answer.

> Participants who dropped out, or who were excluded because they did not receive the index test or
> the reference standard, belong in **Domain 4**, not here.

---

# Domain 2 — Index Test

*Applicability: does the index test as conducted and interpreted match the ideal trial's — cfDNA
from airway fluid supernatant, collected by a reproducibly described technique and genotyped on a
platform with a stated limit of detection?*

### 2.1 — Conducted and interpreted per recommended instructions

**There is no consensus standard for airway liquid biopsy.** The anchor is therefore twofold: the
study's own pre-specified protocol, and the manufacturer's instructions for the extraction kit and
genotyping platform.

Record these seven pre-analytic variables for every study; they are the extraction fields that
decide this answer:

| # | Variable |
|---|---|
| i | Fluid type and instilled volume |
| ii | Whether the bronchoscope was wedged or advanced to the lesion (lesion-directed vs conventional) |
| iii | Time from collection to centrifugation |
| iv | Centrifugation protocol for supernatant separation |
| v | Storage temperature and duration before extraction |
| vi | cfDNA extraction kit and input volume |
| vii | Platform, panel, and stated limit of detection |

| Answer | Rule |
|---|---|
| **Y** | All seven reported, and consistent with the kit/platform instructions. |
| **PY** | (iii)-(v) partly unreported but the specimen was processed fresh within the same session. |
| **PN** | Three or more of (i)-(vii) unreported, with no statement of a standard operating procedure. |
| **N** | A reported deviation likely to degrade cfDNA — e.g. prolonged room-temperature storage before centrifugation, or freeze-thaw of unseparated fluid. |
| **NI** | Specimen handling not described at all. |

**Note.** Unreported pre-analytics are the norm in this literature. Resist collapsing that into NI
across the board: NI is for "cannot judge", PN is for "described enough to see it falls short".

### 2.2 — Interpreted blind to the reference standard

| Answer | Rule |
|---|---|
| **Y** | Explicitly stated that airway genotyping was performed and called blind to the tissue result. |
| **PY** | Airway testing was performed and reported **before** the tissue result existed (temporal blinding), or batched on banked specimens with tissue results not supplied to the laboratory. |
| **PN** | Both performed in the same laboratory with no blinding statement. |
| **N** | The tissue result was available to the laboratory calling the airway result — particularly where a borderline variant call was "confirmed" against tissue. |
| **NI** | Not addressed. |

**Note.** For automated calls above a fixed threshold, blinding matters less; for manual review of
low-VAF variants, it matters a great deal. Weight this answer by which applies.

### 2.3 — Interpreted with the information available in practice

Cuts both ways: **more** information than a practising laboratory would have is as much a problem
as less.

| Answer | Rule |
|---|---|
| **Y** | Called with the clinical and radiological context a laboratory would ordinarily receive, and nothing more. |
| **PY** | Context not described but no indication of extra information. |
| **PN** | Called with the tissue histology and known driver status supplied as context. |
| **N** | Interpretation used information unavailable at the time of testing in practice — e.g. the eventual treatment response, or the final multidisciplinary diagnosis. |
| **NI** | Not addressed. |

### 2.4 — Threshold standard or pre-specified

The threshold in this review is the **variant-calling cutoff**: minimum variant allele fraction,
minimum mutant read or droplet count, and minimum depth of coverage.

| Answer | Rule |
|---|---|
| **Y** | A named cutoff, pre-specified, and consistent with the platform's validated limit of detection. |
| **PY** | The platform's default/validated threshold used without modification. |
| **PN** | A threshold reported but with no statement of when it was set. |
| **N** | **The threshold was chosen to optimise agreement with tissue**, or differed between patients or between arms. Also: a threshold lowered only for the airway specimen and not for plasma in a paired comparison. |
| **NI** | No threshold reported. |

**Note.** N here is close to fatal for the estimate and should usually drive a high domain
judgement, because the estimate is then partly fitted to the reference standard.

---

# Domain 3 — Target Condition

*Applicability: does the target condition as defined by the reference standard match the ideal
trial's — an EGFR mutation (SQ1) or any actionable driver alteration (SQ2) present in the tumour,
as determined by adequate tissue genotyping?*

This is the largest domain (8 questions) and where this review's dominant biases live.

### 3.1 — Reference standard adequately identifies those with and without the condition

| Answer | Rule |
|---|---|
| **Y** | Tissue genotyped on a validated platform whose panel **covers every alteration callable by the index test**, with reported tumour cellularity meeting the platform's minimum. |
| **PY** | Panel coverage matches for the alterations actually analysed in the 2x2, even if narrower overall. |
| **PN** | Tumour content not reported, so a false-negative tissue result cannot be excluded. |
| **N** | **Panel-breadth mismatch** — a single-gene or hotspot PCR tissue reference against a broad NGS airway index. An airway-positive/tissue-negative pair is then uninterpretable as a false positive. |
| **NI** | Tissue platform not described. |

**Note — this is failure mode 2 and it is systematically under-recognised.** Record the tissue
panel and the index panel as separate extraction fields and compare them explicitly. Where they
differ, the estimate is restricted to the **intersection** of the two panels or it is not used.

### 3.2 — Target condition assessed in all participants

**Partial verification. Expected to be the dominant bias in this review.**

| Answer | Rule |
|---|---|
| **Y** | Tissue genotyping attempted in every enrolled participant, with failures reported. |
| **PY** | ≥95% verified, with the unverified accounted for and unrelated to the index result. |
| **PN** | 80-95% verified, or verification status not fully tabulated. |
| **N** | Tissue genotyping performed **only where the airway result was positive**, or only where tissue was judged adequate — i.e. verification depends on the index result or on a correlate of tumour burden. <80% verified. |
| **NI** | Number verified not derivable. |

**Note.** Partial verification inflates sensitivity and deflates specificity. Studies answering N
are excluded in pre-specified sensitivity analysis §9.6(2). Extract the verified/enrolled
denominator explicitly; it is frequently only recoverable from a flow diagram.

### 3.3 — Target condition assessed the same way in all participants

**Differential verification.**

| Answer | Rule |
|---|---|
| **Y** | One tissue platform for all participants. |
| **PY** | More than one platform, but all with equivalent coverage for the analysed alterations and a stated allocation rule. |
| **PN** | Mixed platforms with allocation not described. |
| **N** | Platform assignment tracked specimen adequacy or the index result — e.g. NGS where tissue was plentiful, single-gene PCR where scarce. Distorts both sensitivity and specificity. |
| **NI** | Platform mix not reported. |

### 3.4 — Reference standard avoided incorporating the index test

| Answer | Rule |
|---|---|
| **Y** | Tissue result derived solely from a histological or cytological tumour specimen, independent of the washing supernatant. |
| **PY** | Independent specimens, with the two results reported by different personnel. |
| **PN** | Independence likely but not stated. |
| **N** | **Any of:** (a) a composite "positive by any method" reference that counts the airway result; (b) the comparator genotype derived from the **cell pellet of the same washing** that supplied the supernatant index test; (c) index-positive/tissue-negative cases re-tested on tissue until positive, while index-negative cases were not. |
| **NI** | Provenance of the reference specimen not described. |

**Note — failure mode 4.** Case (b) is specific to this review and easy to miss: pellet and
supernatant are different analytes but the **same** collected fluid, so a tumour-cell-rich washing
makes both results positive together for reasons that have nothing to do with test accuracy. Case
(a) studies are excluded in sensitivity analysis §9.6(3).

### 3.5 — Reference standard conducted and interpreted per instructions

| Answer | Rule |
|---|---|
| **Y** | Accredited laboratory, validated assay, instructions followed. |
| **PY** | Routine clinical diagnostic testing in a hospital laboratory, described but without accreditation detail. |
| **PN** | Research-use assay with no validation reported. |
| **N** | A reported deviation from the assay's instructions. |
| **NI** | Not described. |

### 3.6 — Reference standard interpreted blind to the index test

| Answer | Rule |
|---|---|
| **Y** | Explicit statement of blinding. |
| **PY** | Tissue genotyped as routine care **before** the airway result existed. |
| **PN** | Same laboratory, no blinding statement. |
| **N** | The airway result was known to the pathologist or molecular scientist reading the tissue — especially where it prompted deeper sequencing or a repeat test on tissue. |
| **NI** | Not addressed. |

### 3.7 — Reference standard threshold standard or pre-specified

| Answer | Rule |
|---|---|
| **Y** | Tissue VAF cutoff (and minimum tumour cellularity) named and pre-specified. |
| **PY** | Platform default used unmodified. |
| **PN** | Reported without stating when it was set. |
| **N** | Differed between participants, or was set after seeing the airway results. |
| **NI** | Not reported. |

### 3.8 — Appropriate interval between index test and reference standard

**The ideal is zero** — both specimens from the same bronchoscopy.

| Answer | Rule |
|---|---|
| **Y** | Same procedure, or within 14 days with no intervening systemic therapy. |
| **PY** | Within 90 days, no intervening systemic therapy. |
| **PN** | >90 days with no therapy, or interval not reported in a treatment-naive cohort. |
| **N** | **Any intervening EGFR-TKI or systemic therapy between the two specimens.** Resistance alterations emerge and subclones are lost under treatment, so a discordant pair may reflect real biological change rather than test error. Particularly critical for T790M estimates. |
| **NI** | Interval not derivable. |

**Note.** For post-TKI/resistance cohorts (SQ1 secondary stratum) this question does the most work
in the domain. Extract the interval in days and the treatment given between specimens.

---

# Domain 4 — Analysis

*No applicability judgement — applicability is assessed for domains 1-3 only.*

### 4.1 — All participants included in the analysis

| Answer | Rule |
|---|---|
| **Y** | Every enrolled participant appears in the 2x2 or is accounted for in a flow diagram. |
| **PY** | ≤5% unaccounted, with reasons stated. |
| **PN** | 5-15% dropped, reasons partly stated. |
| **N** | **Participants whose airway cfDNA failed extraction or QC were silently dropped from the 2x2.** This is the single most common analytic problem in this literature: excluding assay failures converts a test-performance limitation into an apparent accuracy gain. |
| **NI** | Enrolled vs analysed numbers not both reported. |

**Note.** The excluded failures are exactly the numerator of our **assay success rate** outcome
(protocol §6.2(3)). Extract them here even when the study discards them, and report the
intent-to-diagnose analysis alongside the per-protocol one.

### 4.2 — Missing data handled appropriately

| Answer | Rule |
|---|---|
| **Y** | Unevaluable index results reported and handled by a pre-specified rule (intent-to-diagnose, or a stated exclusion with a sensitivity analysis). |
| **PY** | Reported and excluded, with numbers given so intent-to-diagnose can be reconstructed. |
| **PN** | Mentioned without numbers. |
| **N** | Unevaluable results counted as negative (or as concordant) without justification. |
| **NI** | Not mentioned. |

### 4.3 — Unit of analysis matches the ideal trial

**The ideal trial's unit is the patient.**

| Answer | Rule |
|---|---|
| **Y** | One 2x2 at patient level; one specimen and one result per patient. |
| **PY** | Multiple specimens per patient, but a pre-specified rule reduces them to one result per patient. |
| **PN** | Unit not clearly stated but patient-level is implied by the denominators. |
| **N** | **Per-alteration or per-specimen pooling** — a patient with three called alterations contributing three rows, or serial specimens from one patient treated as independent. Inflates the effective sample size and understates the confidence interval. |
| **NI** | Denominators inconsistent across outcomes and the unit cannot be determined. |

**Note.** For SQ2 (any actionable driver) the temptation to count alterations rather than patients
is strong. Where a study reports only per-alteration data, it cannot contribute to the
patient-level pool; record it and exclude with full-text code F1.

### 4.4 — Sensitivity and specificity calculated appropriately

| Answer | Rule |
|---|---|
| **Y** | Both computed against the tissue reference with correct denominators, and the 2x2 reproduces the reported figures. |
| **PY** | Cells recoverable and reproduce the reported values within 0.02 (the `dta_extraction_qc.py` tolerance). |
| **PN** | Only sensitivity reported, with specificity omitted but derivable. |
| **N** | **A detection rate reported as sensitivity** — the proportion of airway specimens positive, with no tissue-verified 2x2. Also: sensitivity computed among tissue-positive patients only, with no true-negative cell, presented as diagnostic accuracy. |
| **NI** | Neither the cells nor the denominators are recoverable. |

**Note — failure mode 3, and the reason this review registers assay success rate as a separate
synthesis.** A study answering N here does not contribute to the DTA pool at all (exclusion code
F1); it may still contribute to the proportion synthesis in §6.2(3). Never let a detection rate
enter a sensitivity pool.

---

# QUADAS-C for SQ3 (airway cfDNA vs paired plasma cfDNA)

Applied **in addition to** QUADAS-3, only to studies contributing paired-compartment data.
QUADAS-C was written against QUADAS-2 and is adapted per the QUADAS-3 E&E's preliminary
modifications. An updated QUADAS-C is in development; this section is provisional and will be
re-run against the released tool if it appears before assessment.

**Unit of assessment:** the *comparative* measure — the difference in sensitivity between airway
cfDNA and plasma cfDNA against the same tissue reference. Most primary studies report only the
separate estimate for each compartment, so we compute the comparative measure ourselves; record
which estimate each assessment refers to.

**Domain renaming:** Patient Selection → Participants; Index Test unchanged; Reference Standard →
Target Condition; Flow and Timing → Analysis.

**Three question changes (E&E Table 8):**

| Question | Change |
|---|---|
| C3.2 (reference avoided incorporating any index test) | **Removed** — overlaps QUADAS-3 3.4 |
| C4.2 (appropriate interval between the index tests) | **Moved to Index Test** |
| C4.3 (same reference standard for all index tests) | **Moved to Target Condition** |

**Review-specific rules for the two moved questions:**

- **C4.2 — interval between index tests.** Ideal is same-session: blood drawn during or immediately
  around the bronchoscopy that produced the washing. Y if same day; PY within 7 days with no
  intervening therapy; **N if systemic therapy intervened**, since the compartments then sample
  different disease states and the comparison is confounded by time, not by compartment.
- **C4.3 — same reference standard for both.** Y only if the *same* tissue result served as
  reference for both compartments. N if plasma was compared against one tissue assay and the
  washing against another — a common pattern when plasma testing was clinical and washing testing
  was research.

**Additional comparative concern specific to this review:** the two compartments must be genotyped
on **the same platform with the same calling threshold**. Where the airway specimen was run on a
broad NGS panel and plasma on a hotspot PCR assay, the "compartment" difference is confounded with
an assay difference. Record both platforms; where they differ, the comparison is downgraded and
carried only in a subgroup that states the confound.

**Overall comparative judgement:** low if all domains low; high if any domain high; II if any
domain II and none high.

---

# Recording

One row per assessed estimate in `4_RoB/quadas3_assessments.tsv`, with columns for each of the 20
signalling questions, the four domain judgements, the two applicability judgements (domains 1-3),
the overall risk-of-bias and applicability judgements, and a free-text rationale naming the major
limitations. Per-study per-domain results are reported study-by-study as a traffic-light plot, not
only as pooled proportions (PRISMA item 18).

Where a study contributes more than one estimate (for example SQ1 and SQ2 from the same cohort),
assess the first fully; for subsequent estimates **reassess only the domains whose characteristics
differ**, and record which were carried forward.

---

# Amendments to this appendix

Any change after protocol registration is logged here with date and rationale, and mirrored in the
protocol's amendment table.

| Date | Question | Change | Rationale |
|---|---|---|---|
| — | — | — | — |
