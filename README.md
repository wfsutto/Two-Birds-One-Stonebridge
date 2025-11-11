# Two Birds, One Stonebridge

**Team 2 — Stonebridge**  
Will Sutton, Eric Mueller, Jase Peeler, Joseph Aguilar

## Project Overview

This repository, originally created to contain our Week 7 assignment, serves as the home for our team's Stonebridge Analysis.  

**Stonebridge Task** 

Stonebridge has asked us use Ohio Department of Natural Resources (ODNR) data to evaluate the impact of salt-water injection wells (SWIW) on the state of Ohio's vertical oil drilling and horizontal fracking industry. Given a broad range of questions to research, our group chose to focus on the direct impact of salt-water injection wells on the production of nearby oil and gas wells. Stonebridge representatives expressed concerns voiced by the citizens of Ohio that hazardous brine, produced by the fracking process and disposed of via SWIW, could be impacting the state's groundwater resevoirs. While directly researching the impact of SWIW on the water sources, we are seeking to indirectly evaluate the risk by understanding how SWIW affect nearby production wells. If we find that production wells are hurt by SWIW leaking water or bursting, that indicates that there is a risk that these wells could infect the state's groundwater.

**Week 7 Assignment:** perform exploratory data analysis and a multiple regression on the *Ames Housing* dataset (file: `data/AmesHousing.csv`).  

## Stonebridge Project

In this repository, we can see the following project structure:

```
project-root/
├── data/            # raw and processed data
├── notebooks/       # Jupyter Notebooks
├── results/         # output files (charts, regression results, etc.)
├── README.md        # project description
└── requirements.txt # Python dependencies
```

### Data

Data has been collected on both SWIW and production wells across the states of OH, WV, and PA. Raw data was collected as individual Excel sheets, which are hosted in various subfolders which have been labeled according to the type of data they contain. The final datasets used for analysis are in the `final` subfolder of `data`.

### Reproducing Results

Using the command line, run `pip install -r requirements.txt`. This will install package versions that align our environments.

#### Exploratory Analysis

Next, run the cells in `exploratory_analysis_with_spatial.ipynb` sequentially. This notebook contains the exploratory data analysis stage for all internal OH data. It also goes through the data preparation stage for each created dataset. Lastly, it contains the foundations for our spatial analysis, calculating well locations and plotting them by well type.

##### Expected Outputs

From this, we should expect to see:

1. Cleaned and prepared datasets for annual/quarterly production, permit/plug data, well information, and well owners in the `final` subfolder of `data`
2. Numeric and graphical summaries of production data
3. A plot of all of the wells in OH, colored by whether or not they are SWIW

#### Distance Analysis

Lastly, run the cells in `distance_analysis.ipynb` sequentially. This notebook contains the initial distance analysis, aiming to quantify the relationship between a well's distance to the nearest SWIW and its production. Here, you will find the nearest distance calculation as well as some simple linear regression analysis to quantify the high level relationship between distance and production.

##### Expected Outputs

From this, we should expect to see:

1. Datasets containing API Well Numbers and distance to nearest SWIW and nearest production well
2. Basic SLR outputs, showing both correlation and significance test results

> NOTE: as more analysis is completed, this README will update with instructions on how to replicate the analysis.

## Week 7 - Group Kanban Assignment

In this repository, we can see the following project structure:

```
project-root/
├── data/            # AmesHousing.csv (provided dataset)
├── notebooks/       # Jupyter Notebooks
├── results/         # output files (charts, regression results, etc.)
├── README.md        # project description
└── requirements.txt # Python dependencies
```

In this assignment, we conduct exploratory and regression analysis on Ames Housing data (`AmesHousing.csv`), which is hosted in a subfolder of `data` called `assignment`.

### Instructions

Using the command line, run `pip install -r requirements.txt`. This will install package versions that align our environments.

Then, run the cells in `exploratory_analysis.ipynb` and `regression_analysis.ipynb` sequentially. These two notebooks are located in a subfolder of `notebooks` called `assignment`. This will produce the output of our analysis. Commentary on this analysis can be seen within these files.

Our submission for the Week 7 Assignment can be found in the `results` folder.