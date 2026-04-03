# Sample Reproducible Project

> NOTE: This is a sample project for demonstration purposes. The data and code are not intended for actual research use.

> NOTE: This repository provides a minimal example of a **reproducible research project**.  It demonstrates how to organize files, structure workflows, and document analysis so that results can be fully reproduced from raw data. The project is designed for teaching and demonstration purposes. **This README file provides a template of the README.md file that should be included in a Github repository for a reproducible research project**.

> NOTE: This material is based on the github repository of Prof. Taro Mieno ([click here for the original repository](https://github.com/tmieno2/Sample-Reproducible-Project)), which is created to demonstrate the principles of reproducibility in scientific research in his course. I modified the original material to fit the purpose of this workshop, but the core structure and content are based on his work.

# Overview

This repository contains the full code for the research project: **"The Impact of Weather on Flight Delay"**. 

All results in the manuscript are generated through a reproducible workflow implemented in Quarto and R.

# Project Structure

The main structure of the project is as follows:

```
Sample-Reproducible-Project/
├─ code/          # Scripts for data processing, analysis, and figure generation
├─ data/ 
│  ├─ raw/        # Original, unmodified data
│  ├─ processed/  # Cleaned and processed data used for analysis
├─ results/
│  ├─ figures/    # Generated figures
│  ├─ tables/     # Generated tables 
├─ writing/       # Manuscript and supplementary materials
├─ README.md
├─ Sample-Reproducible-Project.Rproj
```

<!-- Data folder is available from the [xxxx]() data repository. Download the data folder and place it in the correct folder structure (directly under `Sample-Reproducible-Project` folder) as shown above. -->


# How to Reproduce the Project

## Requirements
+ R (version 4.0 or higher)
+ Quarto CLI (https://quarto.org/docs/get-started/)
+ Required R packages are listed in the below. You can install them using the `pacman` package, which will automatically install any missing packages.

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

**Step 1.** Clone the repository to your local machine.

+ Copy the URL of this repository: https://github.com/Shunkei3/Sample-Reproducible-Project.git
+ Rstudio user: File > New Project > Version Control > Git > paste the URL of the repository
+ VScode user: View > Command Palette > Git: Clone > paste the URL of the repository

**Step 2.** Open the `Sample-Reproducible-Project.Rproj` file in RStudio (or set the working directory to the project folder on your other IDE such as VScode). This will ensure that all file paths are correctly set relative to the project directory.

**Step 3.** Follow the instructions in `code/main.qmd` to run the scripts in the correct order. Each script is designed to be run sequentially, and they will generate the results in the `results/` folder.

**Step 4.** To generate the manuscript, render the `writing/manuscript_to_pdf.qmd` file. This will create a PDF version of the manuscript in the `writing/` folder.


## Further Information

*(COMMENT: I avoided describing the details of each script and dataset in the README file to keep it concise and focused on providing an overview of the project and instructions for reproduction. Instead, I provided separate files dedicated to describing the code and data.)*

+ `code/main.qmd` contains the description of each script
+ `data/metadata.md` contains the description of the data source and variable definitions.