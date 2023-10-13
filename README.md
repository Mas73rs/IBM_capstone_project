# Capstone Project:

## Table of Contents
1. [Overview](#overview)
2. [Data Collection](#data-collection)

 
## Overview

The commercial space industry is rapidly growing, with several companies striving to make space travel more affordable and accessible. Among them, SpaceX stands out for its cost-effective approach to rocket launches, mainly due to its ability to reuse the first stage of its Falcon 9 rockets. As a data scientist at Space Y, a new rocket company hoping to compete with SpaceX, your task is to estimate the cost of each rocket launch. This project goes beyond traditional rocket science by utilising machine learning models to predict the probability of a successful first-stage landing, thereby estimating the overall cost of a rocket launch. We will use public information and data visualisation tools to guide this exploration and create internal dashboards for actionable insights. This project encompasses various aspects of data science, including data collection and wrangling, statistical analysis, and predictive modelling. The final presentation will tell the story of the journey and the findings.

## Data Collection

### 1. API
Data for this project was gathered from SpaceX's public API, which provides extensive details on rocket launches, payloads, and landing outcomes. The code for data collection via API can be found below:

[Data Collection via API Notebook.](notebooks/01a_data-collection_api.ipynb)

### 2. Web Scraping
Additional data was collected by scraping information from a Wikipedia page titled [`List of Falcon 9 and Falcon Heavy launches`](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches), contributing to a comprehensive dataset that enriches the analysis. The web scraping code is available below:

[Data Collection via Web Scraping Notebook.](notebooks/01b_data-collection_webscraping.ipynb)

## Data Wrangling

The data wrangling process was an essential step in preparing the SpaceX dataset for analysis and modeling. The process involved the following key steps:

1. **Loading Data**: The SpaceX dataset was loaded from a URL into a pandas DataFrame.
2. **Handling Missing Values**: Calculated the percentage of missing values for each column to identify data issues.
3. **Identifying Data Types**: Determined numerical and categorical columns using data types (`dtypes`).
4. **Summary Statistics**:
    - Calculated launch counts for each site using `value_counts()`.
    - Calculated occurrences of each orbit type and landing outcomes using `value_counts()`.
5. **Data Transformation**:
    - Created a 'Class' column to serve as the label for model training. This was based on the success or failure of landings.
6. **Data Export**: The cleaned and transformed DataFrame was exported to a CSV file for further analysis.

For a more detailed walkthrough, you can refer to this [Data Wrangling Notebook](./notebooks/data-wrangling.ipynb).

This process was crucial for ensuring the quality and reliability of the data, setting the stage for subsequent analysis and modeling.