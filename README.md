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

Next, run the cells in `Data_Processing_and_Well_Inventory.ipynb` sequentially. This notebook contains the exploratory data analysis stage for all internal OH data. It also goes through the data preparation stage for each created dataset, saving them to the `final` subfolder of `data`. Lastly, it contains the foundations for our spatial analysis, calculating well locations and plotting them by well type.

##### Expected Outputs

From this, we should expect to see:

1. Cleaned and prepared datasets for annual/quarterly production, permit/plug data, well information, and well owners in the `final` subfolder of `data`
2. Numeric and graphical summaries of production data
3. A plot of all of the wells in OH, colored by whether or not they are SWIW

#### Distance Analysis

Next, run the cells in `SWIW_Proximity_and_Production_Analysis.ipynb` sequentially. This is the notebook that contains our Difference-in-Differences model comparing production before and after our split point.  The first model output seen is not a DiD, but instead our initial SLR model. This was not used in final analysis.

The first DiD model is for horizontal wells, and it was not part of our final analysis. The next 6 DiD models are for each combination of oil/gas and no-lag/1-year-lag/2-years-lag. The overall model metrics will be at the top of these model summaries, and you can scroll to the bottom to see the individual feature coefficients for the model. The fixed effects can be ignored.

After the 7 DiD models, we created visualizations for each model depicting the change in oil and gas production for each well used in the model dataset. These plots are interactive, and users can zoom in/out, pan, and hover over wells for more information. This feature is helpful to identify wells that can be used in future research.

Lastly, we created line plots summarizing the results of the DiD models. For oil and for gas, we made plots showing the actual and relative production per well, aggregated by the number of relative quarters from the permitting of the nearest SWIW. 

##### Expected Outputs

From this, we should expect to see:

1. Datasets containing API Well Numbers and distance to nearest SWIW and nearest production well
2. Initial basic SLR output
3. Each of the 7 DiD model summaries
4. Four interactive plots showing the difference in production before and after the split date for wells used in the model
5. Four line plots depicting actual and relative production over time relative to the permit date of the nearest SWIW

#### Lag and Seasonal Analysis

Lastly, run the cells in `Seasonal_Trends_and_Lagged_Production.ipynb` sequentially. This notebook was created before the DiD models, and the analysis within was done with the intention to help us select the number of lag years to use in our model and identify basic seasonal trends in the data.

First, we load and aggregate the data as necessary. Then, for each of gas, oil, and brine, we plot the aggregated production by season, as well as a matrix with each of the seasonal averages. Next is a plot of seasonal averages split by distance to the nearest SWIW. We found that the seasonal effects were negligible.

Next, we prepared the annual production data for the lag analysis and trained an OLS model to predict current year production data using lagged production data. We used lags of 1, 2, 3, and 4 years for each of gas and oil. The outputs of all the oil models can be seen first. Then we have a combined model using all four lag effects, then follows a plot of each model's $R^2$ value. Lastly, we see the same outputs for the gas models.

##### Expected Outputs

1. Seasonal aggregate plots for each of oil, gas, and brine
2. Seasonal aggregate matrix
3. Seasonal aggregation split by distance to nearest SWIW plot
4. OLS Model outputs for the 5 models for each of oil and gas (4 individual and 1 combined for each, 10 total models)
5. Plots of each individual model's $R^2$ value for oil and gas

### Results

Our `results` folder includes screenshots of most of the relevant plots used in our analysis. Because the individual well plots for the DiD models are interactive, they were unable to be saved. We also saved the model summaries for each of the 6 DiD models we used in our final analysis. 

Also in this folder, we have included our final presentation, final video, and final writeup.

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