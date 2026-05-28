# Salary Analysis: A Statistical Study Using ANOVA and Regression

**Author:** Vigneshwar Lokoji

## Project Overview

This project analyzes employee salary data using multiple statistical methods to identify which employee characteristics have a significant effect on salary. The analysis progresses from simple to complex models, comparing their explanatory power at each stage.

## Dataset

The dataset contains **789 observations** and **10 variables** covering employee demographics, work experience, performance, and compensation.

**Quantitative Variables:** Salary, ExperienceYears, TrainingHours, PerformanceRating, Age, ProjectsCompleted

**Categorical Variables:** EducationLevel, Department, Gender, JobLevel

## Methodology

### 1. Exploratory Data Analysis
- Histograms for numeric variable distributions
- Boxplots of Salary by each categorical variable
- Correlation matrix and scatterplot matrix to identify predictor relationships

### 2. Simple Linear Regression
`Salary ~ ExperienceYears` — ExperienceYears was identified as the strongest linear predictor of Salary during EDA.

### 3. ANOVA (Analysis of Variance)
`Salary ~ JobLevel` — Tests whether mean salary differs significantly across Junior, Mid, Senior, and Lead levels. Includes Tukey HSD post-hoc comparisons and Bartlett's test for homogeneity of variance.

### 4. Multiple Regression
`Salary ~ ExperienceYears + Age + TrainingHours + PerformanceRating + ProjectsCompleted` — Captures the combined effect of all numeric predictors. Includes VIF analysis to check for multicollinearity.

### 5. ANCOVA (Analysis of Covariance)
`Salary ~ ExperienceYears + JobLevel` — Combines the strongest numeric and categorical predictors to test whether JobLevel affects Salary after controlling for experience.

### 6. Interaction Model
`Salary ~ ExperienceYears * JobLevel` — Tests whether the rate of salary growth per year of experience differs across job levels.

### 7. Model Comparison
All four models are compared using R-squared, Adjusted R-squared, and Residual Standard Error to determine the best-fitting model.

## Technologies Used

- **Language:** R
- **Environment:** Google Colab / Jupyter Notebook
- **Key Techniques:** Linear Regression, ANOVA, ANCOVA, Interaction Modeling, VIF Analysis, Tukey HSD
