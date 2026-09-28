# Delivery

## Two problems

1. **Access** — particle must reach brain interstitial space (cross BBB or bypass it).
2. **Tropism** — once there, it must transfect *microglia*, not merely neurons and astrocytes.

An IVIS glow of the skull after IV luciferase is not a pass. Sorted Tmem119/P2ry12/Hexb or CD11b+CD45int cells with reporter or TREM2 protein is a pass.

```mermaid
flowchart TD
  L[Lipid library] --> IV{IV myeloid over liver}
  IV -->|Acceptable| P[IV commercial path]
  IV -->|Hopeless| CSF{CSF myeloid hit}
  CSF -->|Yes| Q[CSF-facing product]
  CSF -->|No| K[Kill]
```

## Routes

| Route | Role in the program |
|---|---|
| Intravenous | Intended commercial path. Must win or be explicitly deferred. |
| CSF (intracisternal / ICV / lumbar analog) | Scientific control and highest-probability myeloid hit. |
| Intranasal | Backup only if IV and CSF both fail practicality. Mouse nose ≠ human nose. |
| FUS + IV | Out of scope for seed. Device-plus-drug is a different company. |

Decision rule: if IV myeloid/liver exposure is hopeless after the lipid library, **do not** add four antibodies. Switch the label-facing route to CSF or stop.

## LNP composition screen (seed)

**Controls:** DLin-MC3-DMA and SM-102 four-component LNPs (Onpattro / vaccine baselines).

**Test set (20–40 total):**

- Ionizable lipids with published CNS bias (5-HT3-motif, acetylcholine-mimetic, LRP1/BBB-module lipids in the MK16 / OS4T family — synthesize or license, do not invent a 200-lipid campaign).
- Helper lipid and cholesterol ratios (±10 mol%).
- PEG-lipid mol% 0.5–2.5% and two PEG-lipid chain lengths (desorption vs stealth).
- One SORT-style fifth lipid / charge variant if a partner lipid is available.

**Particle specs to hold constant while lipids vary:**

- Diameter 60–100 nm (intensity-weighted)
- PDI ≤ 0.2
- Encapsulation ≥ 80%
- Residual ethanol and empty-particle fraction reported

## Ligands

v1 is **ligand-free** or single small-molecule motif built into the lipid.

Optional v1.1, only if composition is close:

- Mannose (CD206 on activated microglia)
- Anti-CD11b at one density

Do not start with CD34/CD90/c-Kit. Those are HSC markers and the wrong organ.

## Biodistribution interpretation

| Observation | Meaning |
|---|---|
| Liver >> brain, no myeloid signal | Standard LNP. Fail IV. |
| Brain luciferase high, microglia negative | Neuron/astrocyte particle. Fail for TREM2. |
| Endothelium / choroid positive only | Barrier hit, not parenchyma. Fail. |
| Sorted microglia positive, liver acceptable | Pass. Measure TREM2 protein next. |

%ID/g in homogenate is supporting data only.

## Safety labs tied to delivery

Every in-vivo dose cohort:

- ALT, AST, ALP, bilirubin
- Plasma IL-6, IP-10 / CXCL10, TNF, complement Bb or C3a if the assay is available
- Body weight, clinical score
- Spleen and liver histopathology on the top two compositions

Innate activation from the LNP can look like microglial activation. Subtract empty LNP.
