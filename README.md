# Political Trust in the U.S.

## Project Overview
This project is at its developing stage. We are broadly interested in public trust in the U.S. government. Centered around ANES survey data, we explored the correlation between trust and various factors such as demographic characteristics, election outcomes, and economic indicators. Currently, we are using external shocks to explore whether the change in trust is influenced by certain factors such as type of regional industries. 

## Repository Structure

To ensure clarity in the research pipeline, this project is organized into modular directories:

### 1. Data Cleaning & Harmonization (`/01_data_cleaning`)
Contains scripts for processing raw data from the ANES, MIT Election Lab, CBP, and IPUMS NHGIS.
* `01`: Cleans ANES trust and demographic data
* `02`–`03`: Clean and Process election data.
* `04`–`05`: Processes County Business Patterns and NHGIS demographic data.
* `06_merge_data.ipynb`: Merges all sources into a final longitudinal dataset.

### 2. Visualizations (`/02_visuals`)
Contains notebooks focused on secondary data analysis and figure generation.
* `01_time_series.ipynb`: Generates summary tables and trend plots.
* `02_bar_charts.ipynb`: Executes the 2SLS instrumental variables approach and OLS models.
* `03_box_plots.ipynb`: Executes the 2SLS instrumental variables approach and OLS models.

Refer to `codebook.md` for the complete variable names and descriptions.
