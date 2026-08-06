# Multimodal Analysis of Adaptive Immune Features in Down Syndrome 

Code and data-processing workflows supporting the manuscript:  
“Progressive deterioration of adaptive immune repertoires in Down syndrome linked to interferon hyperactivity and lymphoid tissue disorganization”  

------------------------------------------------------------------------

## Overview
* [Repository Structure](#repository-structure-and-table-of_contents)
* [Data Sources](#data-sources)
* [Software & Dependencies](#software--dependencies)
* [R Environment Setup and Running Analyses](#r-environment-setup-and-running-analyses)
* [Citation & License](#citation--license)

------------------------------------------------------------------------

This repository contains code used to analyze datasets from the [Human Trisome Project](https://www.trisome.org/)

It includes:
* R scripts and functions
* Data preprocessing workflows
* Statistical modeling and pipelines
* Reproducibility environment (via renv)
* Documentation for running analyses end-to-end

Each analysis workflow is presented as a self-contained R Project within the main repository. Each project provides a fully reproducible, transparent workflow consistent with open‑science practices.  

------------------------------------------------------------------------

## Repository Structure and Table of Contents

```
ds-adaptive-immune-analysis/
│
├── Analysis_1/            # Self-contained R Project directory for specific analysis workflow
│    ├── Analysis.Rproj          # RStudio project file; double click to open the project in RStudio
│    ├── Analysis_1.R            # Analysis script
│    ├── helper_functions.R      # Associated R functions
│    ├── data/                   # Directory for raw or external data
│    ├── results/                # Directory for results tables, processed data, model outputs
│    ├── figures/                # Directory for visualizations and plots
│    ├── rdata/                  # Directory for workspace images and RDS objects
│    ├── renv.lock               # Lists R package versions for reproducibility
│    └── README.md               # Analysis-specific README
├── .zenodo.json           # Metadata for Zenodo DOI registration
├── LICENSE.md             # Software license
└── README.md              # This README file
```

### Analysis R Projects
* `PROJECT_ONE` - Analysis of DATASET ONE. 
* `PROJECT_TWO` - Analysis of DATASET TWO. 

------------------------------------------------------------------------

## Data Sources
Download each dataset to the appropriate `/data/` directories within each R project.  



### Human Trisome Project (HTP) datasets:  
* Participant-level metadata: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19962380.svg)](https://doi.org/10.5281/zenodo.19962380)
* Visit/Event-level metadata: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19962380.svg)](https://doi.org/10.5281/zenodo.19962380)
* PAXgene whole blood RNAseq data (RPKMs): [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20044079.svg)](https://doi.org/10.5281/zenodo.20044079) and GEO: [GSE190125](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE190125).  
* Plasma proteomics data (SOMAscan): UPDATE[![DOI](). 
* CyTOF Live PLACEHOLDER 
* CyTOF CD45posCD66lo PLACEHOLDER 
* CyTOF B cells PLACEHOLDER 
* BCR PLACEHOLDER
* TCR PLACEHOLDER  
* Tonsil Xenium PLACEHOLDER  


Most of these datasets originate from the Linda Crnic Institute for Down Syndrome's [Human Trisome Project](https://www.trisome.org/) and are also available on the [INCLUDE Data Hub](https://portal.includedcc.org) [DOI: 10.71738/p0a9-2v09](https://doi.org/10.71738/p0a9-2v09).  

------------------------------------------------------------------------

## Software & Dependencies
* [R](https://cran.r-project.org/)  
* [RStudio](https://posit.co/download/rstudio-desktop)  
Key packages include:
* renv
* tidyverse  
* ggplot2  

The renv.lock files within each analysis project directory contains a full list of packages and versions.

------------------------------------------------------------------------

## R Environment Setup and Running Analyses
1. Clone the repository.
   ```
   git clone https://github.com/Linda-Crnic-Institute-for-Down-Syndrome/ds-conditions-multiomics.git
   ``` 
2. Change to desired R Project directory and open R project via `.Rproj` file.
3. Set up reproducible R environment (requires `renv` package to be installed).  

   Option A. Restore the R environment.  
   This will install the exact versions of all R packages but requires matching R version.
   ```
   install.packages("renv")
   renv::restore()
   ```
   Option B. Initialize the R environment.  
   This will install all R packages but will not ensure identical versions.
   ```
   install.packages("renv")
   renv::init(bioconductor = TRUE)
   ```
4. Follow workflow in analysis script.

------------------------------------------------------------------------

## Citation & License
If you use this code, please cite:  
**Manuscript**  
Progressive deterioration of adaptive immune repertoires in Down syndrome linked to interferon hyperactivity and lymphoid tissue disorganization.
Authors, Journal, Year. DOI (UPDATE once available)

**Code**  
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21817536.svg](https://doi.org/10.5281/zenodo.21817536)

This project is licensed under the MIT License – see the LICENSE file for details.
