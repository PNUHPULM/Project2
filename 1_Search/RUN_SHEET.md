# Search run sheet — copy-paste and execute

For the registered search. Run PubMed and Embase, export, and return the files described in
"What to send back". Screening then starts from those exports.

| | PubMed | Embase |
|---|---|---|
| Interface | pubmed.ncbi.nlm.nih.gov — Advanced | embase.com — Advanced Search |
| Form | one combined expression | 22 numbered lines |
| Date limit | inside the expression | line #21 |
| Expected order of magnitude | low hundreds | higher than PubMed (`:ti,ab,kw` is broader, and conference abstracts are indexed) |

---

## 1. PubMed

Paste the whole block into the **Query box** of PubMed Advanced Search (it accepts newlines), or
into the main search bar as one line. Do **not** add any filter from the sidebar — the date limit
is already in the expression, and a sidebar "Humans" filter would drop un-indexed recent records.

```
(
  "Bronchoalveolar Lavage Fluid"[Mesh] OR "Bronchoalveolar Lavage"[Mesh]
  OR "bronchoalveolar lavage"[tiab] OR "BALF"[tiab] OR "BAL fluid"[tiab]
  OR "bronchial washing"[tiab] OR "bronchial washings"[tiab] OR "bronchial wash"[tiab]
  OR "bronchial lavage"[tiab] OR "bronchus lavage"[tiab] OR "airway lavage"[tiab]
  OR "lung lavage"[tiab] OR "targeted washing"[tiab] OR "targeted bronchial washing"[tiab]
  OR "washing fluid"[tiab] OR "lavage fluid"[tiab]
  OR "lavage supernatant"[tiab] OR "washing supernatant"[tiab]
)
AND
(
  "Cell-Free Nucleic Acids"[Mesh] OR "Circulating Tumor DNA"[Mesh] OR "Liquid Biopsy"[Mesh]
  OR "Extracellular Vesicles"[Mesh] OR "Exosomes"[Mesh]
  OR "High-Throughput Nucleotide Sequencing"[Mesh]
  OR "cell-free DNA"[tiab] OR "cell free DNA"[tiab]
  OR "cell-free tumor DNA"[tiab] OR "cell-free tumour DNA"[tiab]
  OR "cfDNA"[tiab] OR "ctDNA"[tiab]
  OR "circulating tumor DNA"[tiab] OR "circulating tumour DNA"[tiab]
  OR "tumor-derived DNA"[tiab] OR "tumour-derived DNA"[tiab]
  OR "liquid biopsy"[tiab] OR "supernatant"[tiab]
  OR "extracellular vesicle"[tiab] OR "extracellular vesicles"[tiab]
  OR "exosome"[tiab] OR "exosomes"[tiab]
  OR "next-generation sequencing"[tiab] OR "next generation sequencing"[tiab] OR "NGS"[tiab]
  OR "targeted sequencing"[tiab] OR "digital PCR"[tiab] OR "ddPCR"[tiab]
  OR "droplet digital"[tiab] OR "PNA clamping"[tiab] OR "peptide nucleic acid"[tiab]
  OR "genotyping"[tiab] OR "molecular profiling"[tiab] OR "genomic profiling"[tiab]
  OR "mutation analysis"[tiab] OR "molecular testing"[tiab] OR "molecular analysis"[tiab]
)
AND
(
  "Lung Neoplasms"[Mesh] OR "Carcinoma, Non-Small-Cell Lung"[Mesh] OR "Adenocarcinoma of Lung"[Mesh]
  OR "lung cancer"[tiab] OR "lung carcinoma"[tiab] OR "NSCLC"[tiab]
  OR "lung neoplasm"[tiab] OR "lung neoplasms"[tiab] OR "lung tumor"[tiab] OR "lung tumour"[tiab]
  OR "pulmonary neoplasm"[tiab] OR "pulmonary carcinoma"[tiab]
  OR "lung adenocarcinoma"[tiab] OR "pulmonary adenocarcinoma"[tiab]
)
AND ("2010/01/01"[Date - Publication] : "3000"[Date - Publication])
```

### Export

`Save` → **All results** → Format **PubMed** (`.txt`) *and* again as **CSV**. Send both.
The PubMed format carries the abstract (needed for title/abstract screening); the CSV carries PMID
and DOI in columns (needed to build the screening sheet).

Also record, before exporting: **the number of results**, and the number **before** the date line
(delete the last `AND (...)` line, note the count, then put it back). Both go in the PRISMA flow.

---

## 2. Embase

Paste line by line into embase.com Advanced Search, recording the count for each. Full rationale
and the Emtree mapping notes are in `1_Search/embase_strategy.md`.

```
#1   'lung lavage'/exp OR 'bronchoalveolar lavage fluid'/exp OR 'bronchus lavage'/exp

#2   'bronchoalveolar lavage':ti,ab,kw OR 'balf':ti,ab,kw
     OR 'bronchial wash*':ti,ab,kw OR 'bronchial lavage':ti,ab,kw
     OR 'bronchus wash*':ti,ab,kw OR 'airway lavage':ti,ab,kw
     OR 'targeted wash*':ti,ab,kw OR 'washing fluid':ti,ab,kw
     OR 'lavage fluid':ti,ab,kw OR 'lavage supernatant':ti,ab,kw

#3   #1 OR #2

#4   (bronchoscop* NEAR/3 (wash* OR lavage)):ti,ab,kw

#5   #3 OR #4

#6   'cell free DNA'/exp OR 'circulating tumor DNA'/exp OR 'liquid biopsy'/exp
     OR 'cell free nucleic acid'/exp OR 'exosome'/exp OR 'extracellular vesicle'/exp

#7   'cell free dna':ti,ab,kw OR 'cell free tumor dna':ti,ab,kw OR 'cfdna':ti,ab,kw
     OR 'ctdna':ti,ab,kw OR 'circulating tumor dna':ti,ab,kw
     OR 'tumor derived dna':ti,ab,kw OR 'liquid biopsy':ti,ab,kw
     OR 'supernatant':ti,ab,kw OR 'extracellular vesicle*':ti,ab,kw OR 'exosom*':ti,ab,kw

#8   #6 OR #7

#9   'high throughput sequencing'/exp OR 'next generation sequencing'/exp
     OR 'digital polymerase chain reaction'/exp OR 'real time polymerase chain reaction'/exp
     OR 'genotyping'/exp OR 'molecular diagnosis'/exp

#10  'next generation sequencing':ti,ab,kw OR 'ngs':ti,ab,kw OR 'targeted sequencing':ti,ab,kw
     OR 'digital pcr':ti,ab,kw OR 'ddpcr':ti,ab,kw OR 'droplet digital':ti,ab,kw
     OR 'pna clamping':ti,ab,kw OR 'peptide nucleic acid':ti,ab,kw
     OR 'genotyping':ti,ab,kw OR 'molecular profiling':ti,ab,kw
     OR 'genomic profiling':ti,ab,kw OR 'mutation analysis':ti,ab,kw

#11  #9 OR #10

#12  'epidermal growth factor receptor'/exp

#13  'egfr':ti,ab,kw OR 'epidermal growth factor receptor':ti,ab,kw
     OR 't790m':ti,ab,kw OR 'exon 19 deletion':ti,ab,kw OR 'l858r':ti,ab,kw
     OR 'driver mutation*':ti,ab,kw OR 'actionable mutation*':ti,ab,kw
     OR 'druggable mutation*':ti,ab,kw OR 'oncogenic driver*':ti,ab,kw
     OR 'mutation*':ti,ab,kw

#14  #12 OR #13

#15  'lung cancer'/exp OR 'non small cell lung cancer'/exp OR 'lung adenocarcinoma'/exp

#16  'lung cancer':ti,ab,kw OR 'nsclc':ti,ab,kw OR 'lung neoplasm*':ti,ab,kw
     OR 'lung carcinoma':ti,ab,kw OR 'lung adenocarcinoma':ti,ab,kw
     OR 'pulmonary neoplasm*':ti,ab,kw

#17  #15 OR #16

#18  #5 AND #8 AND #17

#19  #5 AND #11 AND #14 AND #17

#20  #18 OR #19

#21  #20 AND [2010-2026]/py

#22  #21 NOT ([animals]/lim NOT [humans]/lim)
```

**Final set = #22.** Run both #18 and #19 — the seed gate showed the union is load-bearing.

Check that the count actually drops from #20 to #21. The PubMed MCP interface silently ignored its
date filter in an earlier run, so verify rather than assume.

### Export

Export **#22** → **RIS** *and* **CSV**, with abstracts included. Send both.

---

## 3. Seed gate — run this before sending anything

Search each PMID/DOI inside your result set. **Any miss means the strategy is wrong, not the
seed** — tell me which one and I will diagnose and revise before we screen.

| Seed | PMID | DOI | In PubMed set? | In Embase set? |
|---|---|---|---|---|
| Kim 2026 — targeted washing, EGFR T790M | 40017263 | 10.4143/crt.2024.1128 | ☐ | ☐ |
| Kim 2025 — BWF ctDNA NGS | 40749152 | 10.1200/PO-25-00299 | ☐ | ☐ |
| Murata 2024 — BWF supernatant ddPCR | 38476004 | 10.1093/jjco/hyae021 | ☐ | ☐ |
| Nair 2022 — BAL cfDNA CAPP-Seq | 35748739 | 10.1158/0008-5472.CAN-22-0554 | ☐ | ☐ |
| Ryu 2019 — BW supernatant NGS | 31036768 | 10.1634/theoncologist.2019-0147 | ☐ | ☐ |
| Hur 2018 — BALF EV DNA EGFR | 29374476 | 10.1186/s12943-018-0772-6 | ☐ | ☐ |

## 4. Counts to record (PRISMA identification)

| Item | Value |
|---|---|
| PubMed, before date limit | |
| PubMed, final | |
| Embase #20 (before date limit) | |
| Embase #22 (final) | |
| Date run — PubMed | |
| Date run — Embase | |
| Run by | |

---

## What to send back

1. PubMed export — `.txt` (PubMed format) **and** `.csv`
2. Embase export — `.ris` **and** `.csv`, abstracts included
3. The filled tables in §3 and §4

I deduplicate (DOI → PMID → title+year), build `2_Screening/round1.tsv`, and we start screening.

---

## Verification already done on the PubMed expression

Run against PubMed on 2026-08-26 while drafting.

**All six seeds are retrieved.** This was checked on a *reduced* form of the expression — the
interface used here caps Boolean operators at 20, so the full block above could not be executed
as one query. Every block in the full expression is a **superset** of the corresponding block in
the tested reduced form (same terms plus more, all joined by OR), so the full expression retrieves
at least what the tested form did. That is an argument, not an execution: **still run §3.**

### One finding that changed the expression

The first test returned 58 records and **missed seed 40749152** (the JCO PO bronchial washing
paper). Cause: that abstract writes "cell-free tumor DNA (ctDNA)", and PubMed phrase matching is
exact — `"cell-free DNA"[tiab]` does **not** match "cell-free tumor **tumor** DNA". Adding `ctDNA`
and `"cell-free tumor DNA"` recovered it (62 records).

Both variants, plus `"circulating tumor DNA"`, `"tumor-derived DNA"` and the `-our-` spellings,
are now in the analyte block above, and the equivalents are in Embase line #7. This is exactly the
failure the seed gate exists to catch, and it would have silently removed one of the two most
important studies in the review.

## Not covered by these two databases

Still outstanding for the registered search, per protocol §7.1: Cochrane CENTRAL, Scopus, Web of
Science, ClinicalTrials.gov, WHO ICTRP, and citation chasing on every included study. PRESS peer
review of both blocks should happen before these are treated as the final registered search.
