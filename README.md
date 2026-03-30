# Sample Reproducible Project

*(This repository provides a minimal example of a **reproducible research project**.  It demonstrates how to organize files, structure workflows, and document analysis so that results can be fully reproduced from raw data. The project is designed for teaching and demonstration purposes. This README file provides a template of the README.md file that should be included in a Github repository for a reproducible research project.)*


# Overview

This repository contains the full code for the research project: **"The Impact of Weather on Flight Delay"**. 

All results in the manuscript are generated through a reproducible workflow implemented in Quarto and R.

# Project Structure

The main structure of the project is as follows:

```
Sample-Reproducible-Project/
├─ code/ # Scripts for data processing, analysis, and figure generation
├─ data/ 
│  ├─ raw/        # Original, unmodified data
│  ├─ processsed/ # Cleaned and processed data used for analysis
├─ results/
│  ├─ figures/ # Generated figures
│  ├─ tables/  # Generated tables 
├─ writing/ # Manuscript and supplementary materials
├─ README.md
├─ Sample-Reproducible-Project.Rproj
```

Data folder is available from the [xxxx]() data repository. Download the data and place it in the correct folder structure as shown above.


# Reproducibility

## Requirements
+ R (version 4.0 or higher)
+ Quarto
+ Required R packages:

```{r}
# Run the R code below:
if(!require("pacman")) install.packages("pacman")

pacman::p_load(
  here, 
  rio, 
  data.table, 
  dplyr, 
  fixest, 
  ggplot2, 
  ggtext, 
  modelsummary, 
  flextable,  
  quarto, 
)
```

## Steps to Reproduce Results

step 1. Clone the repository to your local machine.

step 2. Open the `Sample-Reproducible-Project.Rproj` file in RStudio (or set the working directory to the project folder on your other IDE).

step 3. Follow the instructions in `code/main.qmd` to run the scripts in the correct order. Each script is designed to be run sequentially, and they will generate the results in the `results/` folder.

step 4. To generate the manuscript, render the `writing/manuscript_to_pdf.qmd` file. This will create a PDF version of the manuscript in the `writing/` folder.



## Further Information
+ `code/main.qmd` contains the description of each script
+ `data/metadata.md` contains the description of the data source and variable definitions.