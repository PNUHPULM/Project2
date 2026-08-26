# Search strategy — PubMed/MEDLINE

Reported per PRISMA-S (Rethlefsen et al., *Syst Rev* 2021, PMID:33499930).

| Field | Value |
|---|---|
| Database | PubMed/MEDLINE |
| Interface | NCBI E-utilities via the PubMed MCP server |
| Date run | 2026-08-26 |
| Date limits applied | **None applied at the interface** — see Limitation 2 |
| Language limits | None applied at the interface; applied at screening (§5.1) |
| Records retrieved (union) | **182** |
| Status | Scoping/validation run. Not the final registered search — see "Before the registered run" |

## Sub-queries

The strategy is executed as three sub-queries whose results are unioned. The split is forced by
an interface constraint (Limitation 1), not by design; the conceptual strategy is the single
Boolean expression in protocol §7.2.

### QA — analyte block, anchored on a cancer term

```
("bronchoalveolar lavage"[tiab] OR BALF[tiab] OR "bronchial washing"[tiab]
 OR "targeted washing"[tiab] OR "washing fluid"[tiab])
AND ("cell-free DNA"[tiab] OR cfDNA[tiab] OR ctDNA[tiab] OR supernatant[tiab])
AND (cancer[tiab] OR carcinoma[tiab] OR NSCLC[tiab] OR neoplasm[tiab]
     OR tumor[tiab] OR tumour[tiab])
```

Records: **134**

### QB — platform block, anchored on *EGFR*/mutation

```
("bronchoalveolar lavage"[tiab] OR BALF[tiab] OR "bronchial washing"[tiab]
 OR "targeted washing"[tiab] OR "washing fluid"[tiab])
AND ("next-generation sequencing"[tiab] OR NGS[tiab] OR "digital PCR"[tiab]
     OR genotyping[tiab] OR "molecular profiling"[tiab])
AND (EGFR[tiab] OR mutation[tiab])
```

Records: **52**

### QC — extracellular-vesicle block

```
("bronchoalveolar lavage"[tiab] OR BALF[tiab] OR "bronchial washing"[tiab]
 OR "washing fluid"[tiab])
AND ("extracellular vesicle"[tiab] OR exosome[tiab] OR "extracellular vesicles"[tiab])
AND (EGFR[tiab] OR mutation[tiab])
AND lung[tiab]
```

Records: **11**

### Union

| Set | n |
|---|---|
| QA | 134 |
| QB | 52 |
| QC | 11 |
| QA ∩ QB | 7 |
| QA ∩ QC | 5 |
| QB ∩ QC | 6 |
| **Union (deduplicated)** | **182** |

PMID list: `1_Search/pubmed_union_pmids.txt` (one PMID per line, sorted).

## Seed-set retrieval gate — PASS

Protocol §7.2.1. All six seeds retrieved.

| Seed | PMID | Retrieved by |
|---|---|---|
| Kim 2026 — targeted washing, *EGFR* T790M | 40017263 | QB only |
| Kim 2025 — BWF ctDNA NGS | 40749152 | QA |
| Murata 2024 — BWF supernatant cfDNA ddPCR | 38476004 | QA, QB |
| Nair 2022 — BAL cfDNA CAPP-Seq | 35748739 | QA only |
| Ryu 2019 — BW supernatant ultra-deep NGS | 31036768 | QA only |
| Hur 2018 — BALF EV DNA *EGFR* | 29374476 | QA, QB, QC |

**No single sub-query retrieves all six.** The union is load-bearing: dropping QB loses the
targeted-washing seed, dropping QA loses Nair and Ryu. Any amendment that removes a sub-block
must re-run this gate before execution.

## Interface limitations found during this run

These are properties of the MCP interface used here, not of PubMed, and they must be worked
around before the registered search is run.

1. **Boolean operator cap (max 20).** The single combined expression in protocol §7.2 (30
   operators) is rejected. Hence the three-way split above. The union is mathematically
   equivalent to the intended `A AND B AND (C OR D)` only for the term sets actually included —
   so the registered run must either be executed in the native PubMed web interface (no cap) or
   the split must be reported as executed, with the union counts, exactly as done here.
2. **`date_from` appears not to be applied.** A `date_from=2010` filter was passed on every
   query, yet the QA result set contains records from the 1990s and earlier. The 2010 date limit
   in protocol §5.1 must therefore be applied **at the interface in the registered run**, or
   enforced at screening and reported as a screening exclusion rather than a search limit. Do
   not assume the filter took effect.
3. **Result-set truncation.** `max_results` caps at 100 per call; QA required pagination
   (`retstart=100`) to retrieve all 134. Any re-run must paginate to the reported `total_count`.

## Before the registered run

- Re-execute in the native PubMed interface with the full §7.2 expression and MeSH terms
  (`"Bronchoalveolar Lavage Fluid"[MeSH]`, `"Cell-Free Nucleic Acids"[MeSH]`,
  `"Carcinoma, Non-Small-Cell Lung"[MeSH]`), which this run did not include.
- Apply the 2010 date limit at the interface and confirm it took effect.
- PRESS peer review.
- Then execute Embase (Emtree), Cochrane CENTRAL, Scopus, and Web of Science, and re-record
  counts here per database.

The 182 records above are a **scoping result**, not the PRISMA identification count. The PRISMA
flow starts from the registered run.
