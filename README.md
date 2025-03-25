# Group 2 Adult Census Income Exploratory Analysis Project

## Overview
The team chose to analyze adult census income data consisting approximately 48K instances from the 1994 census database. This dataset was donated to UC Irvine Machine Learning Repository in 4/30/1996. 

## Objectives
- The main objective is to predict whether income exceeds $50K/yr using the census data. 
- We will be using Supervised Machine Learning Model: Logistic Regression, Random Forest Classifier, and Gradient Boosting Classifier.

## Prerequisites and Data References:
- UC Irvine Machine Learning Repository [Data source](https://archive.ics.uci.edu/dataset/20/census+income).
- There are 2 datasets from UCI: adult.data and adult.test. We combine both datasets into census_combined.csv. 
- Store the csv file in /resources/ folder.
- All files will need to be run in Jupyter Notebook.

## Activities
- To minimize unbalance of the data categorize each column to specific classification. Optimal Binning library approach is used against the manual categorization/binning to see which one produces better results. Example of how we do the manual binning is like classifying age below 30 years old as "young", age between 30-50 years old as "middle age", and age above 50 years old as "old".
- Data cleanup work includes: removing duplicates data, removing records with '?' aka null data, removing records for those Non-United-States native-country . Columns that are deemed to be extra noise and therefore are not necessary are dropped: relationship (which is already represented in marital-status), education-num (which is already represented in education), and native-country (since all records retained now are only United-States origin).

## File(s) to Run
- [Exploration Exchange Rate](https://github.com/AIBC2024/Group-2-Census-Income/blob/main/Group_2_Census_Income_ML_Model.ipynb)

## Summary of the Final Analysis
- TBD after we are done with the Jupy notebook file.

## Team Members
1. [Ingrid Blankevoort](https://github.com/AIBC2024)
2. [Matt Le](https://github.com/mattledevs)
3. [Patrick McCourt](https://github.com/patrickjm7)
4. [Spencer Gerritsen](https://github.com/sppencerr)
5. [Vijay Srinivasula](https://github.com/vijaysrini-1982)

## Google Slide Deck Presentation
[Group presentation link](https://docs.google.com/presentation/d/1c5HKskr5M4CTCZ3icPqyk4lvaxkg8-hCKdf96O0XVI8/edit?usp=sharing) 
