# AL002 clinical data (competitor constraint)

Human TREM2 *occupancy* has been tested. NVL-101 is copy-number. Do not argue with these numbers; design around them. Primary sources: INVOKE-1 (*Alzheimers Res Ther* 2024; PMID 39444037); INVOKE-2 (*Nat Med* 2026; PMID 41787076; NCT04592874); Alector 25 Nov 2024 PR; ClinicalTrials.gov results posted Oct 2025.

## Molecule

AL002 (Alector): humanized **IgG1 TREM2 agonist mAb**. Binds TREM2, clusters/internalizes receptor, **lowers** membrane TREM2 and shed sTREM2. IV q4 weeks. Not an anti-amyloid mAb.

## INVOKE-1 — Phase 1, healthy volunteers (NCT03635047)

- n = 64 SAD, 0.003–60 mg/kg IV vs placebo.
- Tolerated. No treatment-related SAEs over 12 weeks. Headache 36%, nausea 17% on drug.
- CSF/serum ~0.07–0.28% (typical mAb).
- **CSF sTREM2:** dose-dependent drop; **max 63% vs placebo on Day 3 at 60 mg/kg**; still −32% from baseline at Day 30 at 60 mg/kg.
- Downstream CSF: osteopontin/SPP1, sCSF1R, IL-1RA/IL1RN up (microglia-activation panel).
- NHP: weekly IV to 250 mg/kg × 4 weeks tolerated; CSF sTREM2 −>70% at 80 and 250 mg/kg; **total TREM2 protein down** in hippocampus and cortex (internalization).

Implication: sTREM2 *fall* is the occupancy PD. NVL-101, if it works, should *raise* surface TREM2 and may raise sTREM2. Same marker, opposite direction. Do not copy AL002’s PD success criterion.

## INVOKE-2 — Phase 2, early AD (NCT04592874)

### Design

- Randomized, double-blind, placebo-controlled, 1:1:1:1.
- AL002 **15 / 40 / 60 mg/kg IV q4 weeks** for 48–96 weeks.
- Population: early AD, amyloid+ (PET or CSF), CDR-GS 0.5–1, MMSE ≥20 (protocol language varied slightly by source), age 50–85.
- *Nat Med* reports **381** randomized. ClinicalTrials.gov **actual enrollment 356**. FAS in registry results: placebo 88, 15 mg/kg 97, 40 mg/kg 94, 60 mg/kg 77. Fifteen **APOE ε4/ε4** were enrolled in Part 1, then **permanently excluded** for ARIA severity and dropped from FAS.
- Sites: North/South America, Europe, Australia, NZ. Completed Sep 2024. LTE stopped after the readout.

### Efficacy (primary failed)

CDR-SB change from baseline vs placebo at week 96 (MMRM, *Nat Med* abstract):

| Arm | LSM difference vs placebo (95% CI) |
|---|---|
| 15 mg/kg | −0.31 (−1.61 to 0.98) |
| 40 mg/kg | +0.13 (−1.18 to 1.43) |
| 60 mg/kg | −0.17 (−1.49 to 1.15) |

All *P* > 0.05. Intervals include both benefit and harm. No dose trend.

Alector 25 Nov 2024: **no benefit** on secondary clinical/functional endpoints, **no favorable AD fluid biomarkers**, **no treatment-related amyloid PET reduction**. One extended-data PET note at week 48 in the 40 mg/kg arm was a nominal SUVR flicker, not a clearance story.

### Pharmacodynamics (worked)

Sustained CSF **sTREM2 down**, CSF **osteopontin up**. Target engagement and a microglia PD signal in patients — the same pattern as Phase 1. Engagement ≠ clinical benefit.

### Safety (class-defining)

ClinicalTrials.gov “other AEs” (approximate; treat as source of record for rates):

| Event | 15 mg/kg n=97 | 40 mg/kg n=94 | 60 mg/kg n=77 | Placebo n=88 |
|---|---|---|---|---|
| ARIA-E | 21 (22%) | 22 (23%) | 17 (22%) | 1 (1%) |
| ARIA-H | 28 (29%) | 28 (30%) | 21 (27%) | 4 (5%) |
| SAE any | 14 (14%) | 12 (13%) | 10 (13%) | 7 (8%) |
| Death | 1 | 1 | 1 | 1 |

Alector 2023 blinded update (includes early ε4/ε4): ARIA-E **8/15 (71%)** in ε4/ε4 vs **41/206 (27%)** after they were pulled; ARIA-H same 71% vs 29%. In the remaining population most ARIA-E was asymptomatic (~88% in that snapshot); serious ARIA ~1%. Infusion reactions dose-related.

ARIA was **not** lower at lower amyloid burden (opinion/secondary analyses). Timing: often first 3 months; some ARIA-H reported months after last dose.

## What this does to NVL-101

1. **Occupancy of existing TREM2 is not an untested alternative.** It was tested at three doses for up to 96 weeks and missed every clinical and amyloid-PET bar that matters.
2. **CSF marker movement is not a Phase 2 ticket.** AL002 moved sTREM2 and osteopontin. Copy that PD and you have copied a failed program’s surrogate.
3. **ARIA-like MRI is a TREM2-activation risk, not only an anti-amyloid risk.** APOE ε4/ε4 is a hard human lesson. FIH concept must look like an anti-amyloid MRI schedule.
4. **PD direction differs.** Agonist: sTREM2 ↓ (internalization). mRNA: surface TREM2 should ↑; sTREM2 may ↑. If NVL-101 only drops sTREM2, you have built a sloppy agonist.
5. **Enrichment AL002 did not use:** TREM2 hypomorphic carriers. That is the only genetic slice where “more receptor” is not just louder occupancy.
6. **Do not combo with lecanemab/donanemab in FIH.** Two myeloid/amyloid-vessel hits stacked is how you design an ARIA trial.

## Open questions the papers do not close

- Was microglia activation on CAA vessels the ARIA mechanism? Plausible, not proven.
- Would an earlier, TREM2-variant, or CSF-delivered copy-number approach evade ARIA? Unknown.
- Sanofi oral TREM2 agonist SAR448851 is heading to Phase 2 (TREMHANCE) *after* this miss. Oral occupancy is not a rescue of the human hypothesis; it is another occupancy test.
