# Assays and decision numbers

Numbered notes point to [references.md](references.md).

## Cascade

```mermaid
flowchart TD
  Q[mRNA QC] --> D[iPSC-microglia protein and function]
  D -->|Pass Aim 1| R[Reporter LNP IV vs CSF]
  D -->|Kill| Z[Stop]
  R -->|Sorted myeloid hit Aim 2| T[TREM2 LNP in WT then 5xFAD]
  R -->|No myeloid| Z
  T --> X[Repeat-dose tox]
```

Do not skip to Morris water maze.

## In vitro panel

| Assay | Platform | Pass (working) |
|---|---|---|
| mRNA integrity | Capillary electrophoresis | Single major peak, % intact ≥ 80 |
| TREM2 mRNA | qPCR, 6–24 h | ≥5× vs untreated |
| Surface TREM2 | Flow, clone that sees human ectodomain | ≥2× MFI vs empty LNP at 24–48 h |
| Total TREM2 / sTREM2 | ELISA or MSD | Directionally up; report both |
| pSYK | Phospho-flow or blot after lipid ligand | Increase vs empty LNP[[4]](references.md) |
| Aβ phagocytosis | pHrodo or fluorescent Aβ | ≥50% relative increase vs empty LNP |
| Viability | ATP + Annexin | ≥70% of untreated at the passing dose |
| ISG / IFN | qPCR (IFIT1, MX1, RSAD2) | Empty LNP subtracted[[8]](references.md) |

Use **human iPSC-microglia** as the decision line.

Include a TREM2-R47H iPSC line or knockdown/rescue if available.[[2]](references.md) That separates copy-number from generic activation.

## In vivo panel

| Assay | Pass (working) |
|---|---|---|
| Sorted microglia reporter | Significant vs vehicle and vs MC3 control[[10]](references.md) |
| Sorted microglia TREM2 protein | Detectable increase vs empty LNP |
| Liver luciferase or mRNA | Reported as a ratio |
| ALT/AST | ≤3× vehicle mean unless histopathology is clean |
| Cytokines 2–6 h and 24 h | Document |
| Plaque metrics (only after exposure pass) | 6E10 / methoxy-X04 area, microglial clustering[[5]](references.md)[[11]](references.md) |

DAM transcripts in sorted microglia are supporting, not a substitute for protein.[[6]](references.md)

## What is out of scope until exposure exists

- Cognition batteries as primary
- Multi-omics atlases as a substitute for protein
- Non-human primate before a mouse myeloid pass

## Controls (non-negotiable)

- Vehicle
- Empty LNP (same lipids, no RNA)
- Irrelevant mRNA LNP
- MC3 or SM-102 TREM2 mRNA (standard particle, same cargo)[[10]](references.md)
