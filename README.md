# Adult Income Dataset Analysis

## Overview
This project involves data cleaning and exploratory statistical analysis of the Adult (Census Income) dataset. The goal is to clean messy real-world data and explore probability distributions (PMF, PDF, CDF) on key features.

## Dataset
This project uses the Adult/Census Income dataset from the UCI Machine Learning Repository (https://archive.ics.uci.edu/dataset/2/adult), containing 48,842 instances with demographic and employment-related attributes.

The dataset is fetched directly in the notebook using:

from ucimlrepo import fetch_ucirepo
adult = fetch_ucirepo(id=2)

## Project Steps

### 1. Data Cleaning
- Identified and handled missing values disguised as '?' in workclass, occupation, and native-country columns
- Filled missing categorical values with 'Unknown'
- Detected and handled a capped value (99999) in capital-gain, creating a separate flag feature (capital-gain-capped)
- Fixed inconsistent labels in the income column (<=50K. vs <=50K)
- Checked for outliers in numerical columns (age, fnlwgt, hours-per-week) using boxplots and the IQR method

### 2. Exploratory Statistical Analysis
- PMF (Probability Mass Function): Analyzed the probability distribution of education levels
- PDF (Probability Density Function): Fitted a normal distribution to age and compared it with the actual histogram
- CDF (Cumulative Distribution Function): Computed the empirical CDF of age to answer questions such as "what percentage of individuals are under 40 years old?"
- Measured skewness to confirm the right-skewed nature of the age distribution

## Key Findings
- The age distribution is right-skewed (skewness approximately 0.56), with the mean (38.64) greater than the median (37.00)
- About 56.19% of individuals are under 40 years old
- The most common education level is High School graduate (approximately 32% of the population)

## Tools and Libraries
- Python
- pandas
- numpy
- matplotlib
- scipy

## Requirements
pandas
numpy
matplotlib
scipy
ucimlrepo

Install with:
pip install -r requirements.txt

## How to Run
1. Clone this repository
2. Install dependencies
3. Open the notebook file in Jupyter Notebook
4. Run all cells in order

## Author
Anita
