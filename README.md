# Two Birds, One Stonebridge

**Team 2 — Stonebridge**  
Will Sutton, Eric Mueller, Jase Peeler, Joseph Aguilar

## Project overview

This repository hosts a short reproducible analysis for Week 7 and will serve as the foundation for our semester-long group project.  
**Current assignment:** perform exploratory data analysis and a multiple regression on the *Ames Housing* dataset (file: `data/AmesHousing.csv`).  

> NOTE: Our long-term consulting goal is to analyze injection well incidents for Stonebridge. For the Week 7 assignment we are using the Ames Housing dataset to demonstrate reproducible workflows and modeling steps. The README will be updated once the Stonebridge dataset and project scope are finalized.

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

In this assignment, we conduct exploratory and regression analysis on Ames Housing data (`AmesHousing.csv`).

### Instructions

Using the command line, run `pip install -r requirements.txt`. This will install package versions that align our environments.

Then, run the cells in `exploratory_analysis.ipynb` and `regression_analysis.ipynb` sequentially. This will produce the output of our analysis. Commentary on this analysis can be seen within these files.