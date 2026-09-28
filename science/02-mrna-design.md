# TREM2 mRNA design

## Construct architecture (v0.1)

```
[Cap 1 analog] — [5' UTR] — [Kozak] — [human TREM2 CDS] — [3' UTR] — [polyA]
```

- **CDS:** NP_061838 / NM_018965.4 isoform 1 (canonical 230 aa), wild type. No R47H. Include native signal peptide so the protein enters the secretory path and reaches the plasma membrane.
- **Codon optimization:** human microglia-biased codon table; remove cryptic splice sites and extreme GC runs; do **not** strip all rare codons if that slows folding of the Ig domain.
- **UTRs:** start with a documented high-expression pair used in therapeutic mRNA (e.g. human α-globin or proprietary equivalents from the CDMO). Screen 2–3 UTR pairs in iPSC-microglia; pick by protein, not by luciferase in HEK293.
- **Cap:** CleanCap AG or equivalent Cap 1. Cap 0 is not acceptable for innate-immune reasons.
- **Nucleotides:** N1-methylpseudouridine (ψ) as default; run an unmodified-U arm if ψ depresses TREM2 trafficking (empirical).
- **polyA:** 80–120 A, templated or enzymatic, with a defined length release spec.
- **dsRNA:** cellulose or enzymatic depletion; release test by immunoassay. dsRNA is the usual cause of “the LNP looks inflammatory.”

## What we will not put on the mRNA in v1

- IRES or dual cistrons (TREM2 + BDNF, TREM2 + DAP12).
- Destabilizing tags or inducible switches.
- Genome-editing ORFs.

DAP12 is already abundant in microglia. Do not complicate v1 by co-expressing the adaptor unless dish data show DAP12 is limiting.

## Sequence documentation (for CMC later)

Maintain in `assets/data/` when generated:

- FASTA of optimized CDS + UTRs
- Annotation of residual restriction sites, uORFs, and CpG islands
- In vitro transcription template map (plasmid vs linear dsDNA)
- Identity tests: Sanger or NGS of template; capillary electrophoresis of mRNA; capping efficiency; polyA length distribution

## Expression kinetics (expected, to be measured)

| Time after transfection | Expectation |
|---|---|
| 4–8 h | mRNA detectable |
| 12–24 h | Surface TREM2 up |
| 48–72 h | Peak protein / phagocytosis window |
| 5–10 d | Protein back toward baseline in dividing cultures; longer in vivo if cells are quiescent |

Redose interval in animals will be set by the decay curve, not by analogy to COVID vaccines.

## Immunogenicity of the payload

TREM2 is a self protein. The mRNA product should not look like a foreign antigen if the amino-acid sequence is human WT. Remaining innate risk is the **particle and residual dsRNA**, not the TREM2 peptide. Still run anti-TREM2 Ig after repeat mouse doses in case of misfolded protein.
