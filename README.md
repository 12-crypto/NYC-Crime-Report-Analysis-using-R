# NYC Crime Trend Analysis 

A comprehensive statistical computing project analyzing NYC crime complaint data using exploratory data analysis and machine learning techniques to predict crime patterns across NYC boroughs.
<img width="242" height="213" alt="image" src="https://github.com/user-attachments/assets/6303b253-d9b1-4321-b1f3-44cc73ff95d9" />


## Dataset Overview

**Source**: NYPD Complaint Data Current YTD  
**Records**: 361,740 records across 5 NYC boroughs  
**Time Span**: Current year-to-date NYC crime complaints  
**Format**: Structured CSV with geographic, temporal, and incident-level features

## Preprocessing Highlights

- Handled missing values in coordinate and complaint data
- Removed unnecessary columns (`PARKS_NM`, `HADEVELOPT`) 
- Converted character variables to numeric factors for ML compatibility
- Engineered temporal features (hour, day-of-week, month)
- Applied 70-30 train-test split with random sampling
- Final cleaned dataset: 355,625 records with 18 features

## Research Questions & Models

### 1️⃣ **Borough Crime Prediction**
*Multi-class classification predicting NYC boroughs from crime features*

- Models: Random Forest, Decision Tree, Logistic Regression, k-NN, SVM
- Best Accuracy: **99.12%** (Random Forest)
- Best AUC: **0.993** (multiclass)
- Use: Geographic crime pattern analysis and resource allocation

### 2️⃣ **Drug Crime Analysis**
*Statistical breakdown of dangerous drug offenses*

- Found: **50.35%** of drug crimes involve marijuana
- Most Common: Marijuana possession (4 & 5) with 8,121 cases
- Use: Targeted enforcement and policy development

### 3️⃣ **Temporal Crime Patterns**
*Time-series analysis of crime occurrence patterns*

- Heatmap analysis by hour × day-of-week
- Monthly crime distribution trends
- Peak hours and seasonal variation identification
- Use: Optimal patrol scheduling and prevention strategies

## Exploratory Data Analysis (EDA)

- Borough distribution: Brooklyn (29.4%), Manhattan (24.1%), Bronx (22.2%)
- Crime categories: Misdemeanor (55.0%), Felony (31.0%), Violation (14.0%)
- Geographic density mapping using hexbin visualization
- Chi-squared tests confirming borough-crime associations
- Coordinate-based spatial analysis and outlier detection

## Tools & Technologies

**Language**: R  
**Libraries**: `tidyverse`, `ggplot2`, `caret`, `randomForest`, `e1071`, `rpart`, `nnet`, `pROC`, `viridis`, `corrplot`  
**Methods**: Classification, Statistical Testing, Geospatial Analysis, Data Visualization

## Key Takeaways

- Geographic coordinates (X_COORD_CD, Y_COORD_CD) are the most predictive features for borough classification
- Random Forest significantly outperforms other algorithms with 99.12% accuracy
- Clear temporal patterns exist that can inform law enforcement scheduling
- Statistical tests confirm significant associations between boroughs and crime types

## Limitations & Future Work

- SVM computational constraints required dataset reduction for feasible training
- Potential for real-time data integration and automated crime forecasting
- Integration of weather data and special events for enhanced prediction accuracy
- Development of interactive dashboard for stakeholder engagement
