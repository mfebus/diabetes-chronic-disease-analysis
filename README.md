# SIADS 593: Milestone I

## **Exploring Diabetes and Chronic Disease Rates Across U.S. States**
#### **Maria Febus, Dung Hoang, & Sara Jahanian | Winter 2026**



### **Background**
According to the Centers for Disease Control and Prevention (2024), approximately 38 million people in the United States have diabetes, which is frequently observed alongside other chronic diseases such as cardiovascular disease and COPD. These co-occurring rates differ between states.

### **Motivation** 
The purpose of this project is to conduct an exploratory data analysis (EDA) to:
Evaluate relationships and uncover patterns between diabetes and other chronic diseases at the state level.
Provide insight into groups that are disproportionately affected and the factors driving this disparity. 
Our aim is to inform and guide data scientists onboarding to this project about how we utilize data science methods to discover and share insights that can lead to the development of more effective and efficient healthcare strategies and policies to better serve the individuals in our society. 

### **Questions**
What chronic diseases are associated with higher diabetes prevalence at the state level?
Which state-level socioeconomic factors ( such as income, employment, and insurance access), and local characteristics are most strongly associated with diabetes prevalence across U.S. states?
Scope 
- Population: Adults 18 and over
- Timeframe: 2022
- Location: U.S. States
- State-Level Metrics: 2022 U.S. Census Data
- Chronic Diseases Covered: Diabetes, obesity, asthma, arthritis, and chronic obstructive pulmonary disease (COPD) rates 
- Granularity: One row per U.S. State

## Project Structure
This repository contains a modular Python data pipeline designed to load, clean, transform, analyze, and visualize structured datasets. The workflow is orchestrated through a Jupyter Notebook and supported by reusable Python modules for data loading, wrangling, and visualization.

```
├── main.ipynb          # Orchestrates the end-to-end workflow
├── lib/
│   ├── Data_loader.py      # Functions for loading and saving data
│   ├── Data_wrangle.py     # Data cleaning, transformation, and processing logic
│   ├── visual2.py          # Plot generation and visualization formatting
├── data/
│   ├── raw/            # Raw input datasets
│   └── processed/      # Cleaned and processed outputs
└── README.md

```
## File Descriptions
### main.ipynb - Orchestrator
The main notebook serves as a control center for the project.

* Imports fuctions from the supporting Python Modules.
* Loads raw datasets.
* Applies data cleaning and transformation steps.
* Merges processed datasets.
* Generates visualizations.

### data_loader.py - Data Loading & Saving
This module centralizes all inputs/output operations.

* Loading CSV files into pandas DataFrames.
* Saving processed DataFrames back to disk as a CSV file.

### data_wrangle.py - Data Cleaning & Transformation
This module contains the core data-processing logic.

* Adding, removing, and renaming columns.
* Filtering rows and columns based on criteria.
* Handleing missing values.
* Coverting data types.
* Data specific transformations.
* Merging and reshaping datasets for analysis.

### visual2.py - Visualization
This module is responsbile for all visual outputs.

* Creating histograms, boxplots, and correlation plots.
* Formatting visual elements for readability and consistency

## Typical Workflow
1. Run main.ipynb
2. Load raw data using functions from data_loader.py
3. Clean, transform, and merge data using data_wrangle.py
4. Save processed DataFrames using data_loader.py
5. Generate plots and visuals using visual2.py

## Dependencies
This project relies on common Python libraries.

* sys
* os
* pandas
* numpy
* matplotlib
* seaborn
* jupyter

## Getting Started
1. Clone the repository:
   * Open GitHub Desktop.
   * Click File -> Clone Repository.
   * In the dialog: URL tab: Paste the repository URL (e.g., https://github.com/username/repo.git).
   * Click Clone.
   * GitHub Desktop will download the repository and set it up locally.
2. Install required dependencies.
3. Open main.ipynb in Jyupter.
4. Run the Notebook from top to bottom.


## Jupyter Auto‑Reloading (Recommended)

This project is meant to be run from main.ipynb while you edit the other .py files. The notebook uses Jupyter’s autoreload feature so your changes show up automatically.

### Why Autoreload?
Normally, if you change a .py file, Jupyter won’t notice unless you restart the notebook. Autoreload fixes this by automatically picking up changes when you run a cell.
Although restarting the kernel achieves the same result, this apporach is recommened.

### Commands Used

```
%reload_ext autoreload
%autoreload 2
```
