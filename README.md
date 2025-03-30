# Group 2 Adult Census Income Exploratory Analysis Project

## Overview
The team chose to analyze adult census income data consisting approximately 48K instances from the 1994 census database. This dataset was donated to UC Irvine Machine Learning Repository in 4/30/1996. 

## Objectives
- The main objective is to predict whether income exceeds $50K/yr using the census data. 
- Use Supervised Machine Learning Model. For example: Logistic Regression, Random Forest Classifier, Gradient Boosting Classifier.

## Prerequisites and Data References:
- UC Irvine Machine Learning Repository [Data source](https://archive.ics.uci.edu/dataset/20/census+income).
- There are 2 datasets from UCI: adult.data and adult.test. We **combine** both datasets into census_combined.csv. 
- Store the csv file in /resources/ folder.
- All files will need to be run in Jupyter Notebook.

## Activities
- To minimize unbalance of the data categorize each column to specific classification. Optimal Binning library approach is used against the manual categorization/binning to see which one produces better results. Example of how we do the manual binning is like classifying age below 30 years old as "young", age between 30-50 years old as "middle age", and age above 50 years old as "old". More details are shown on the [presentation link](https://docs.google.com/presentation/d/18lDUSq6sC4JHum-QVp4FL4gWg8F2ANKATeriCumoacQ/edit?usp=sharing).
- Data cleanup preparation includes: removing duplicates data, removing records with '?' aka null data, removing records for those Non-United-States native-country . Columns that are deemed to be extra noise and therefore are not necessary are dropped: relationship (which is already represented in marital-status), education-num (which is already represented in education), native-country (since all records retained now are only United-States origin), and fnlwgt.
- Create basic visualization for the combined dataset to understand any possible biases or imbalaned. The line chart does not represent any forecasting. It only shows the total count, ordered from the highest count to the lowest count for each column category.
- Create Variance Inflation Factor (VIF) test to assess multicolinearity. The end result shows there are no multicolinearity on this dataset after the data cleanup activities.
- Perform train, test, split for supervised ML model: GradientBoostingClassifier, ExtraTreesClassifier, RandomForestClassifier, DecisionTreeClassifier, KNeighborsClassifier, AdaBoostClassifier, LogisiticRegression. The end result shows that **GradientBoostingClassifier** and **XGBoost** are the most 2 optimal models.
- Perform Hyperparameter Tuning for the lowest 2 models: KNeighbors and LogisticRegression, check ROC AUC Score. They don't perform any better.
- Perform Feature Importance analysis: the end result shows the order of: (1) marital-status, (2) assets, (3) education, (4) occupation, (5) age, (6) hours per week, (7) sex, (8) workclass, and (9) race.
- Perform Learning Curves to check overfitting.
- Perform SMOTE resample analysis at GradientBoostingClassifier.
- Inspect Model Coefficients. The end results show the top 4 most influencing features are: (1) marital-status, (2) occupation, (3) education, and (4) hours per week. 
- Perform Correlation Matrix analysis: similarly as Model Coefficients and Feature Importance analysis, the top 3 most influencing features are: (1) marital-status, (2) education, (3) age
- Perform Granular Correlation for impactful factors in determining whether income exceeds $50k/year based on the 1994 census database: marital-status, education, age, race

## File(s) to Run
- [Exploration Exchange Rate](https://github.com/AIBC2024/Group-2-Census-Income/blob/main/Group_2_Census_Income_ML_Model.ipynb)

## Summary of the Final Analysis
- Higher income ($50K/year) are influenced by some factors such as: marital status (married has higher income), type of education (having a bachelor degree+), occupation (white collar has higher income).
- Top best performing models are: GradientBoostingClassifier and XGBoost with train and test models are in the mid 80%, ROC/AUC in upper 80%/low90%, no overfitting/underfitting

## Team Members
1. [Ingrid Blankevoort](https://github.com/AIBC2024)
2. [Matt Le](https://github.com/mattledevs)
3. [Patrick McCourt](https://github.com/patrickjm7)
4. [Spencer Gerritsen](https://github.com/sppencerr)
5. [Vijay Srinivasula](https://github.com/vijaysrini-1982)

## Google Slide Deck Presentation
[Group presentation link](https://docs.google.com/presentation/d/18lDUSq6sC4JHum-QVp4FL4gWg8F2ANKATeriCumoacQ/edit?usp=sharing) 
