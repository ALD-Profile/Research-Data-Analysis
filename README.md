# Research-Data-Analysis
Codes used to process LUTO2 output data and for figure preparation.

## Overview

This repository contains the Jupyter notebooks used to extract, organize, prepare, validate and analyze outputs from the Land-Use Trade-Offs Model Version 2 (LUTO2) for a national scale study of renewable energy siting and biodiversity exposure in Australia.

The analysis examined 16 LUTO2 scenario configurations combining alternative energy, emissions and biodiversity settings. The notebooks in this repository were used to process LUTO2 model outputs, create analysis ready datasets, validate extracted records and prepare data used in the figures and summary tables presented in the study.


## Study context

The study compares 16 LUTO2 scenario configurations generated from three scenario dimensions:

- **Energy pathway**
  - Step Change
  - Accelerated Transition

- **Emissions setting**
  - Flexible
  - Strict

- **Biodiversity setting**
  - Baseline
  - Habitat Avoidance
  - Restoration
  - Habitat Avoidance + Restoration

The reference configuration is **S-01: Step Change + Flexible + Baseline**.

The analysis focuses on modelled **Utility Solar PV** and **Onshore Wind** development and examines renewable generation, modelled land allocation, nationally significant biodiversity exposure and land-use transition costs.

The broader study evaluates renewable energy outputs from 2030 to 2050 and biodiversity exposure under the 16 configurations, with particular attention to Species of National Environmental Significance (SNES) and Ecological Communities of National Environmental Significance (ECNES).


## Repository contents

The notebooks are numbered broadly according to their role in the data processing and analysis workflow.

| Notebook | Purpose |
|---|---|
| `01-Data-Inventory.ipynb` | Inspects and consolidates CSV outputs from individual LUTO2 scenario runs and records file level audit information. |
| `02-Model-run-settings-summary.ipynb` | Extracts and summarises the model settings associated with the 16 LUTO2 runs. |
| `03-Figure 3-Renewable generation and land allocation.ipynb` | Validates and analyzes renewable generation and modelled land allocation data and prepares the comparative renewable energy figure. |
| `04-SNES-ECNES-data.ipynb` | Extracts, consolidates and validates LUTO2 biodiversity output files for SNES and ECNES across all 16 runs and analysis years. |
| `05-Transition-data.ipynb` | Extracts, standardizes, validates and summarizes LUTO2 land-use transition area and cost outputs across all 16 scenario runs. |


## Workflow

The notebooks form a post processing workflow applied to LUTO2 model outputs.

The general workflow is:

```text
LUTO2 scenario outputs
        │
        ▼
01 — Data inventory and output audit
        │
        ▼
02 — Model run settings verification
        │
        ├────────► 03 — Renewable generation and land allocation
        │
        ├────────► 04 — SNES and ECNES data preparation
        │
        └────────► 05 — Land-use transition data preparation
                         │
                         ▼
               Analysis-ready datasets
                         │
                         ▼
                Figures and tables



## Data validation and quality assurance

Validation checks were incorporated throughout the processing workflow. These included checks for expected scenario runs and years, required output files, missing or duplicate records, file and row count completeness, numeric data validity, preservation of scenario and source identifiers, and potential double counting of aggregate records.

The original LUTO2 outputs were retained unchanged, while processed datasets preserved run and source information to support traceability.


## Outputs

The notebooks generate processed datasets, validation records and figure ready summaries used in the study. These outputs support analysis of renewable generation, modeled land allocation, SNES and ECNES exposure, scenario sensitivity and land-use transition costs.

## Code development

AI assisted code development: ChatGPT codex and Claude was used to assist with code structure and debugging, used to organize LUTO2 model outputs. All code was reviewed, modified and tested by the author before use. The scripts do not generate or alter LUTO2 optimization results.

## Software

The notebooks were developed in Python using Jupyter Notebook, with packages including pandas, NumPy, Matplotlib and openpyxl.


## Data access and file paths

The notebooks were developed using a Windows based project directory. Local paths may need to be updated before running the notebooks on another computer.

The required LUTO2 scenario outputs are not necessarily included in this repository because of file size and data management considerations.


## Interpretation

Renewable energy outputs represent modeled LUTO2 allocations rather than approved or final renewable energy projects.

Biodiversity exposure represents association with modeled renewable allocation and should not be interpreted as direct evidence of realized ecological impact.

Land-use transition costs represent modeled LUTO2 land-use and land management transition costs rather than observed renewable infrastructure expenditure or total electricity-system costs.


LUTO2
The underlying model used in this research is:

Land-Use Trade-Offs Model Version 2 (LUTO2)
https://github.com/land-use-trade-offs/luto-2.0

LUTO2 is a separate open-source model. This repository contains post processing and analysis code developed for the present study.


Citation
If you use or refer to the analysis workflow in this repository, please cite the archived version of the repository.

Suggested citation format:
Delgado, A. (2026). Research data analysis: LUTO2 renewable energy and biodiversity scenario analysis (Version 1.0.0) [Computer software]. GitHub. https://github.com/ALD-Profile/Research-Data-Analysis




