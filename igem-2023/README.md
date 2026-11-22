# CAPBSULEC | Mathematical Modeling of a Synthetic Biology System for Lead Capture

**iGEM UNMSM · iGEM Design League 2022 · Mathematical modeling research**  
**Institution:** Universidad Nacional Mayor de San Marcos (UNMSM), Peru  
**My role:** Mathematical Modeling Lead — Diego Salazar  
**Project type:** Team research project; computational and theoretical modeling

> **Project documentation, not a runnable code repository.** This page summarizes the mathematical modeling work described in the team's *Results of the Mathematical Modeling Area* technical report. The original simulation source code is not included. All treatment-related outcomes discussed here are **theoretical model predictions**, not experimental or clinical evidence of efficacy.

## Overview

**CAPBSULEC** was a proposed synthetic-biology approach to reducing gastrointestinal lead absorption. The concept involved producing a recombinant human metallothionein (MT1A)-based protein with a regulated genetic circuit in *Escherichia coli*, then using a capsule-based delivery strategy to bind lead in the gastrointestinal tract.

The mathematical modeling area examined whether the proposed biological design could plausibly support controlled protein expression, bacterial production, lead binding, and the anticipated downstream effects of reducing lead uptake. Modeling was used to explore design trade-offs and assumptions **in silico**, before any claims about real-world efficacy could be made.

## My Contribution

I led the mathematical modeling work for the iGEM UNMSM team. My responsibilities included developing and evaluating quantitative models and using their predictions to inform the proposed biological design. The technical report covers five connected lines of analysis:

1. Genetic circuit dynamics and robustness.
2. Bacterial growth and bioreactor operation.
3. Metallothionein–lead binding affinity.
4. Gastrointestinal lead-capture kinetics.
5. Theoretical changes in lead distribution following reduced ingestion/absorption.

This was a collaborative synthetic biology project. The description here highlights my modeling contributions without implying sole authorship of the overall project.

## Modeling Work

### 1. Genetic circuit dynamics: regulation, stability, and noise

**Question:** Could the proposed circuit switch reliably between low and high expression of recombinant MT1A while remaining robust to fluctuations in gene expression?

The models examined a **Lac/Tet regulatory toggle switch**, **T7 RNA polymerase-mediated expression**, and inhibition involving the **T7 RNA polymerase–lysozyme complex**. The report documents:

- Deterministic differential-equation models of successive circuit designs, including transcription, translation, complex formation, and protein degradation.
- A reduced two-variable formulation used to explore equilibria and the **bistability** of the regulatory switch.
- Stochastic simulations to investigate gene-expression noise and compare alternative strategies for changing expression levels.
- Iterative design changes intended to increase MT1A production in the **ON** state while limiting unwanted production in the **OFF** state.

**Reported findings:** Early versions displayed switch-like behavior but insufficient recombinant-protein expression relative to regulatory proteins. Reducing translation rates and modifying circuit parameters helped preserve distinct expression states. In later versions, the addition of the **LysS/T7 lysozyme** regulatory mechanism reduced simulated background expression in the OFF state.

**Report:** Section 1, pp. 3–12; circuit parameters and equations in the appendix, pp. 29–37.

### 2. Bioreactor growth and operating conditions

**Question:** How could bacterial biomass and substrate availability change during cycles of protein production in a chemostat?

A simplified continuous-culture model represented *E. coli* biomass growth as a function of limiting substrate concentration and dilution rate. It explored changes between growth and production periods, incorporating assumptions about growth reduction and toxicity when recombinant-protein expression was activated.

**Reported findings:** Simulated changes in dilution rate could help sustain biomass across production cycles and avoid substrate depletion under the selected assumptions. Some effects, including growth penalties and toxicity, were represented using **illustrative/arbitrary parameters**, explicitly identified in the report as quantities requiring future empirical measurement.

**Report:** Section 2, pp. 13–17.

### 3. Metallothionein–lead affinity under gastrointestinal conditions

**Question:** How might the affinity of human MT1A for lead vary with **pH** and **temperature** when direct binding measurements were scarce?

The approach combined literature-derived information on metallothionein binding to other metals and related metallothionein proteins. The report estimated binding parameters for five binding steps and transformed these estimates across pH and temperature conditions relevant to the proposed application.

**Reported findings:** The resulting affinity surfaces supplied parameters for the downstream lead-capture model. Because lead-specific measurements for human MT1A were limited, these affinity values were **inferred**, rather than directly experimentally measured for the proposed system.

**Report:** Section 3, pp. 18–21.

### 4. Lead-capture kinetics in gastrointestinal compartments

**Question:** Given the proposed protein release and lead-binding behavior, how could free lead concentrations change in the gastrointestinal tract?

The model combined assumptions about protein release from a porous microcapsule, concentrations of MT1A and lead in the **stomach and duodenum**, intestinal flow, and chemical species formed as lead binds metallothionein. The report describes using **GNU Octave** to calculate the distribution of lead-bound MT1A species from simulated concentrations.

**Reported findings:** The modeled system predicted lower free-lead concentrations when MT1A was included than in a comparison scenario without it. Under the report's chosen assumptions, one logarithmic-scale comparison showed differences on the order of **10^12** in simulated free-lead concentration over much of the modeled duodenal pathway. This numerical result is a **model output**, not an experimentally observed effect or clinical treatment claim.

**Report:** Section 4, pp. 22–24.

### 5. Theoretical lead distribution over time

**Question:** What changes in tissue lead burden might be expected if gastrointestinal lead uptake were reduced over an extended period?

The report extended the proposed mechanism using a literature-based model of lead distribution across body compartments, simulating long-term changes for several assumed intake scenarios.

**Reported findings:** The simulations suggested reductions in modeled tissue lead burden after the hypothetical intervention. These results remain conditional on the preceding assumptions about delivery, binding, and reduced uptake; **no clinical validation is claimed**.

**Report:** Detoxification Process section, pp. 25–26.

## Methods and Tools

| Area | Methods / tools documented |
| --- | --- |
| Scientific computing | **Python** (genetic circuit modeling), **GNU Octave** (chemical species distribution) |
| Dynamical systems | Deterministic differential equations, equilibrium and stability analysis |
| Biological variability | Stochastic gene-expression simulations and noise analysis |
| Bioprocess modeling | Chemostat growth models, substrate and dilution-rate dynamics |
| Biochemical modeling | Binding affinity estimation, pH/temperature transformations, chemical equilibrium |
| Physiological modeling | Two-compartment gastrointestinal simulations and literature-based lead-distribution scenarios |

The specific Python packages and their versions cannot be verified from the available report, so no environment file or installation instructions are provided here.

## What This Project Demonstrates

- Translating a multidisciplinary biological proposal into **explicit mathematical assumptions and testable models**.
- Comparing alternative genetic circuit designs with **deterministic and stochastic simulations**.
- Using modeling to identify design trade-offs and to guide discussion with other research areas.
- Combining models across biological scales, from **gene expression to gastrointestinal chemical binding**.
- Clearly separating **literature-derived parameters, illustrative assumptions, and computational predictions**.

## Recognition and Project Timeline

The iGEM UNMSM team received a **Gold Medal at iGEM Design League 2022** for the CAPBSULEC proposal. The current portfolio folder is named `igem-2023` for consistency with the owner's existing organization, but the **competition award was in 2022**, not 2023. Project-related dissemination and technical documentation also appeared in 2023.

## Attribution

**Mathematical Modeling Lead:** Diego Salazar  
**Project team:** iGEM UNMSM, Universidad Nacional Mayor de San Marcos, Peru

The overall CAPBSULEC concept and project were collaborative team efforts. Prior studies underlying individual model assumptions are cited in the original technical report.
