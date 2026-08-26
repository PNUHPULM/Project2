# Search strategy — Embase (Emtree)

Reported per PRISMA-S. **Status: drafted, NOT executed.**

| Field | Value |
|---|---|
| Database | Embase (Elsevier) |
| Interface | embase.com — Advanced Search |
| Drafted | 2026-08-26 |
| Executed | **Not yet** — see "Why this is not executed" |
| Records retrieved | — |

## Why this is not executed

Neither route into Embase is available from this session:

1. **No Embase MCP connector exists.** The MCP registry has no Embase or Elsevier server.
2. **Direct access is blocked.** `api.elsevier.com`, `www.embase.com`, and `api.embase.com` are all
   refused at the egress proxy.
3. **An Elsevier API key would not be sufficient anyway.** Elsevier's own support documentation
   excludes Embase (with Reaxys, SciVal and PharmaPendium) from the APIs available at no charge to
   academic researchers, and the Embase API additionally requires institutional IP authentication
   or an Institutional Token issued manually by Elsevier — not generated in the developer portal.

Embase must therefore be run by the review team or an institutional medical librarian on a
subscribed account. That is the ordinary systematic-review workflow: PRESS recommends the search be
developed with a librarian regardless.

**Hand-off:** run the block below, then return (a) the result count per line, (b) the final union
count, and (c) whether each of the six seeds in §"Seed gate" was retrieved. Those numbers are
filled into this file and the protocol's §7.2.1 gate is re-run.

## Emtree mapping notes

The PubMed strategy is not transferable line-for-line. Substantive differences found while mapping:

| Concept | PubMed | Embase | Consequence |
|---|---|---|---|
| Airway lavage | `"Bronchoalveolar Lavage Fluid"[MeSH]` | Emtree preferred term is **`lung lavage`**; `bronchoalveolar lavage fluid` maps as a narrower/related term | Explode `'lung lavage'/exp` **and** keep `'bronchoalveolar lavage fluid'/exp` — neither alone covers the other |
| Bronchial washing | free text only | `'bronchus lavage'/exp` exists as an Emtree term | Adds indexed retrieval PubMed cannot match |
| Cell-free DNA | `"Cell-Free Nucleic Acids"[MeSH]` | `'cell free DNA'/exp` and `'circulating tumor DNA'/exp` are **separate** Emtree terms, not nested as in MeSH | Both must be listed explicitly; exploding one does not pull the other |
| Liquid biopsy | free text | `'liquid biopsy'/exp` is an indexed Emtree term | Adds indexed retrieval |
| NSCLC | `"Carcinoma, Non-Small-Cell Lung"[MeSH]` | `'non small cell lung cancer'/exp` | Direct equivalent |
| Truncation | none used | `*` (e.g. `wash*`) | Enables `washing`/`washings`/`washed` in one term |
| Adjacency | none | `NEAR/n`, `NEXT/n` | Used in line 4 to catch un-indexed phrasings |
| Field tags | `[tiab]` | `:ti,ab,kw` (keyword field has no PubMed equivalent) | Broader than `[tiab]` — expect a higher yield than PubMed's 182 |

Two consequences to expect: Embase indexes conference abstracts heavily (excluded at screening
under code E4, but they inflate the identification count and must be reported), and `:ti,ab,kw`
retrieves more than `[tiab]`, so the Embase line count will exceed the PubMed one.

## Search block

Run as numbered lines so each count can be reported (PRISMA-S).

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

#7   'cell free dna':ti,ab,kw OR 'cfdna':ti,ab,kw OR 'ctdna':ti,ab,kw
     OR 'cell-free tumor dna':ti,ab,kw OR 'liquid biopsy':ti,ab,kw
     OR 'supernatant':ti,ab,kw OR 'extracellular vesicle*':ti,ab,kw
     OR 'exosom*':ti,ab,kw

#8   #6 OR #7

#9   'high throughput sequencing'/exp OR 'next generation sequencing'/exp
     OR 'digital polymerase chain reaction'/exp OR 'real time polymerase chain reaction'/exp
     OR 'genotyping'/exp OR 'molecular diagnosis'/exp

#10  'next generation sequencing':ti,ab,kw OR 'ngs':ti,ab,kw
     OR 'digital pcr':ti,ab,kw OR 'ddpcr':ti,ab,kw OR 'droplet digital':ti,ab,kw
     OR 'pna clamping':ti,ab,kw OR 'peptide nucleic acid':ti,ab,kw
     OR 'genotyping':ti,ab,kw OR 'molecular profiling':ti,ab,kw
     OR 'genomic profiling':ti,ab,kw OR 'mutation analysis':ti,ab,kw

#11  #9 OR #10

#12  'epidermal growth factor receptor'/exp OR 'protein kinase inhibitor'/exp

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

**Final set: #22.**

### Structure and why it mirrors PubMed

Lines #18 and #19 are the Embase equivalents of the PubMed sub-queries QA (analyte block) and QB
(platform block). The PubMed seed gate showed the union is load-bearing — QB alone retrieved the
targeted-washing seed, QA alone retrieved Nair and Ryu — so **both lines must be run and unioned at
#20**. Do not run #18 alone.

The extracellular-vesicle terms sit inside #6/#7 rather than in a third line, because Embase's
`'extracellular vesicle'/exp` is indexed and does not need the separate rescue query that PubMed's
QC provided.

No DTA methodological filter is applied: such filters are known to lose eligible records, and the
topic blocks are already narrow.

### Line #22 — animal exclusion

The `NOT ([animals]/lim NOT [humans]/lim)` construction removes animal-only records while keeping
records indexed for both. Do **not** use a bare `NOT [animals]/lim`, which discards human studies
that also report animal work.

### Line #21 — date limit

`[2010-2026]/py` applies the protocol §5.1 date floor at the interface. **Confirm the count drops
between #20 and #21.** In the PubMed run the interface's date filter was silently ignored and
1990s records survived a 2010 limit; verify rather than assume.

## Seed gate (to run after execution)

Protocol §7.2.1. Check whether each is in set #22. Any miss sends the strategy back for revision
before the search is used, and the revision is logged here.

| Seed | PMID | DOI |
|---|---|---|
| Kim 2026 — targeted washing, *EGFR* T790M | 40017263 | 10.4143/crt.2024.1128 |
| Kim 2025 — BWF ctDNA NGS | 40749152 | 10.1200/PO-25-00299 |
| Murata 2024 — BWF supernatant cfDNA ddPCR | 38476004 | 10.1093/jjco/hyae021 |
| Nair 2022 — BAL cfDNA CAPP-Seq | 35748739 | 10.1158/0008-5472.CAN-22-0554 |
| Ryu 2019 — BW supernatant NGS | 31036768 | 10.1634/theoncologist.2019-0147 |
| Hur 2018 — BALF EV DNA *EGFR* | 29374476 | 10.1186/s12943-018-0772-6 |

If a seed is missed, check in this order: (1) is it indexed in Embase at all — some Korean and
Japanese journals are not; (2) does it fail #5 (airway block) or #17 (population block); (3) is the
missing term one that Emtree indexes under a preferred term not listed above. Record the diagnosis,
not just the fix.

## Results table (to fill on execution)

| Line | Concept | n |
|---|---|---|
| #5 | Airway specimen | |
| #8 | Analyte | |
| #11 | Platform | |
| #14 | Target condition | |
| #17 | Population | |
| #18 | Analyte route (≈ PubMed QA) | |
| #19 | Platform route (≈ PubMed QB) | |
| #20 | Union | |
| #21 | + date limit | |
| **#22** | **+ animal exclusion — final** | |

Date run: ______  Run by: ______  Interface: embase.com Advanced Search

## Still outstanding for this database

- PRESS peer review of this block before it is used for the registered search.
- Decide with the librarian whether Embase conference abstracts are exported (they are excluded at
  screening under E4, but PRISMA requires them in the identification count if retrieved).
- Deduplicate against the PubMed set by DOI first, then PMID, then title+year (protocol §7.1).
