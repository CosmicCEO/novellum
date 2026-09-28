# TREM2 mRNA design

Numbered notes point to [references.md](references.md).

## Construct architecture (v0.1)

```
[Cap 1 analog] — [5' UTR] — [Kozak] — [human TREM2 CDS] — [3' UTR] — [polyA]
```

- **CDS:** NP_061838 / NM_018965.4 isoform 1 (canonical 230 aa), wild type. No R47H.[[1]](references.md)[[2]](references.md) Include native signal peptide so the protein enters the secretory path and reaches the plasma membrane.
- **Codon optimization:** human-biased codon table; remove cryptic splice sites and extreme GC runs.
- **UTRs:** start with a documented high-expression pair used in therapeutic mRNA. Screen 2–3 UTR pairs in iPSC-microglia; pick by protein, not by luciferase in HEK293.
- **Cap:** CleanCap AG or equivalent Cap 1.
- **Nucleotides:** N1-methylpseudouridine as default. Modified nucleosides reduce TLR recognition of in vitro RNA.[[8]](references.md)[[9]](references.md)
- **polyA:** 80–120 A, templated or enzymatic, with a defined length release spec.
- **dsRNA:** cellulose or enzymatic depletion; release test by immunoassay.

## What we will not put on the mRNA in v1

- IRES or dual cistrons (TREM2 + BDNF, TREM2 + DAP12).
- Destabilizing tags or inducible switches.
- Genome-editing ORFs.

DAP12 is already abundant in microglia.[[7]](references.md) Do not co-express the adaptor in v1 unless dish data show it is limiting.

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
| 5–10 d | Protein back toward baseline in dividing cultures |

Redose interval in animals will be set by the decay curve, not by vaccine analogy.[[9]](references.md)

## Immunogenicity of the payload

TREM2 is a self protein. Remaining innate risk is the **particle and residual dsRNA**, not the TREM2 peptide.[[8]](references.md) Still run anti-TREM2 Ig after repeat mouse doses in case of misfolded protein.
