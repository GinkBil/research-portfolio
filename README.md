# Diego Salazar | Computational Biology Research Portfolio

**Computational biology · Population genetics · Mathematical modeling · Scientific Python**

I am a computational biologist with an MSc in Biosciences from the **University of Oslo** and a BSc in Genetics and Biotechnology from the **National University of San Marcos**. My research focuses on using computational models, simulations, and quantitative methods to investigate biological questions.

This portfolio brings together scientific code from my master's research and selected documentation of mathematical modeling projects in synthetic biology. It also summarizes research experience whose code and data cannot be shared publicly.

## Featured Projects

### 1. GWAS Power Simulation — Master's Research (2026)

**Field:** Population genetics, evolutionary genomics, statistical genetics  
**Tools:** Python, SLiM, tskit, pyslim, msprime, PLINK, GEMMA, NumPy, pandas, SciPy

Developed a simulation-based workflow to investigate how sample size, genetic architecture, and population structure affect the detection of causal genetic variants in genome-wide association studies (GWAS).

The workflow combines forward-time population simulation, tree-sequence recapitation, neutral mutation overlay, genotype and quantitative phenotype generation, and association testing with linear mixed models. It also records significant associations and distinguishes causal signals from associations outside specified causal windows.

**My contribution:** Designed the simulation workflow, implemented Python analysis functions, integrated bioinformatics tools, and evaluated statistical behavior across simulated scenarios.

**Code:** [GWAS Power Simulation repository](https://github.com/GinkBil/gwas-power-simulation)

### 2. Capbsulec — Mathematical Modeling for Synthetic Biology (iGEM UNMSM, 2023)

**Field:** Synthetic biology, dynamical systems, biochemical modeling  
**Methods:** Deterministic and stochastic models, differential equations, numerical simulation

Worked on mathematical modeling for **Capbsulec**, a proposed synthetic-biology approach to limiting lead exposure using metallothionein-based binding. The modeling report documents several interconnected components:

- **Genetic circuit dynamics:** Modeling a regulatory switch and recombinant protein expression, including stability and stochastic noise.
- **Bioreactor growth:** Simulating bacterial biomass, substrate availability, and operating conditions in a chemostat.
- **Metallothionein–lead affinity:** Estimating binding behavior under different pH and temperature conditions using literature-derived assumptions.
- **Capture kinetics:** Modeling protein release and lead-binding dynamics in gastrointestinal compartments, with additional theoretical simulations of lead distribution.

**My contribution:** Led the mathematical modeling work, developing and evaluating quantitative models to inform the project's biological design.

**Documentation:** [iGEM 2023 project overview](igem-2023/README.md). The underlying report contains theoretical predictions and should not be interpreted as clinical validation.

### 3. LactIQ — Mathematical Modeling for Continuous Lactate Monitoring (iGEM UiOslo-Norway, 2025)

**Field:** Computational physiology, biosensors, sports science  
**Methods:** Mathematical modeling, physiological parameter analysis

Contributed to **LactIQ**, an interdisciplinary project exploring a wearable biosensor for continuous lactate monitoring in athletes. I developed the project's mathematical modeling component, examining how lactate levels change in the body and the detection requirements relevant to the proposed sensor.

**My contribution:** Independently developed the mathematical modeling section documented on the team's official iGEM wiki.

**Documentation:** [Modeling page on the official iGEM 2025 wiki](https://2025.igem.wiki/uioslo-norway/model) · [Project overview](https://2025.igem.wiki/uioslo-norway/description)

## Additional Research Experience — Non-public Materials

The following projects involved restricted research environments or human-related data. **No datasets, unpublished results, or internal project code are included in this portfolio.**

- **Computational Physiology & Machine Learning — Simula / UC San Diego (2025):** Applied machine learning to cardiac mechanics parameter prediction in a summer research program.
- **Epidemiological Data Analysis — University of Oslo, Department of Pharmacy (2026):** Developed reproducible workflows for comparing observational study configurations using restricted healthcare registry data.

## Research Methods & Tools

| Area | Experience |
| --- | --- |
| Scientific programming | Python, R, Jupyter, NumPy, pandas, SciPy, Matplotlib, scikit-learn |
| Computational genomics | SLiM, tskit, pyslim, msprime, PLINK, GEMMA |
| Quantitative biology | Genome simulations, statistical power analysis, GWAS, mathematical modeling, stochastic and deterministic systems |
| Research workflows | Experimental design, data analysis, validation against theoretical expectations, technical documentation |

## Selected Scientific Presentations

- **Island Biology Conference (2026), Atami, Japan:** *Development of an Automated Simulation Pipeline for Sample Size and Statistical Power Estimation in Association Studies*.
- **Society for Molecular Biology and Evolution (2026), Copenhagen, Denmark:** *Evaluating GWAS Statistical Power for Causal Genes Discovery Using Genome Simulations*.

## Availability & Attribution

The **GWAS** project is presented as a code-based research project; the **iGEM** projects are documented research contributions, with original source code not currently included here. Research materials developed in collaboration with teams remain attributable to those teams. Public documentation is linked where available, and any additional files are shared only when redistribution is permitted.

## Contact

**Diego Salazar**  
Email: [diego.salazarct@gmail.com](mailto:diego.salazarct@gmail.com)
