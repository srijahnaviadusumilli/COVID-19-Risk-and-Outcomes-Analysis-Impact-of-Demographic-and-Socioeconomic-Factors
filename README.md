# COVID-19 Risk and Outcomes Analysis Impact of Demographic and-Socioeconomic Factors
This repository contains materials for the project "Analyzing the Impact of Demographic, Socioeconomic, and Racial Factors on COVID-19 Risk and Outcomes in U.S. Counties", which investigates how socioeconomic disparities and demographic characteristics influenced COVID-19 outcomes across 3,142 U.S. counties. Using comprehensive statistical analysis and regression modeling, the project reveals critical health disparities and provides evidence-based insights for public health policy.

## Project Overview

- **Objective**:  Examine the relationships between poverty, race, demographic characteristics, and COVID-19 outcomes to understand pandemic disparities and inform equitable public health interventions.

- **Data Source**: COVID-19 Race, Gender, and Poverty Risk Dataset - comprehensive county-level data from USA Facts, U.S. Census, CDC, and Policy Map (https://www.kaggle.com/datasets/laurindogarcia/covid-19-race-gender-poverty-risk-us-county).
  
- **Sample Size**: 3,142 U.S. counties with 21 variables covering socioeconomic, demographic, and health factors.

- **Research Questions**:
How do socioeconomic, racial, and demographic factors impact cumulative COVID-19 deaths?
How do these factors influence health risk categorizations across counties and states? 
  
- **Approach**:
Comprehensive exploratory data analysis with visualization techniques.
Statistical analysis using non-parametric methods (Kruskal-Wallis, Chi-square tests).
Linear regression for predicting COVID-19 deaths.
Logistic regression for health risk category classification.
Correlation analysis using Spearman's rank correlation.

## Key Findings
- **Health Disparities**
Strong correlation between poverty rates and COVID-19 mortality across U.S. counties
Disproportionate impact on counties with larger minority populations and higher poverty rates
Counties with larger Black and Hispanic populations showed higher case and death rates
- **Model Performance**
Linear Regression: Explained 85% of death variability (adjusted R² = 0.8475)
Logistic Regression: Achieved 98.53% accuracy in predicting county health risk categories
Confidence Interval: 97.13% to 99.36% for logistic model reliability

## Files in the Repository

- **covid19-analysis-.Rmd-**: R Markdown file containing complete statistical analysis pipeline.
- **covid19-analysis-report.pdf-**: Full research report with methodology, results, and policy implications.
- **covid19-analysis-presentation.pptx-**: Slide deck summarizing key findings, methodology, and clinical relevance.
  
## Methodology

- **Data Collection & Preprocessing**
  - Missing Data Assessment: Verified no null values using `colSums(is.na(data))`
  - Variable Selection: Removed 3 irrelevant columns, focused on 21 clinically relevant variables
  - Outlier Treatment: Applied IQR method for robust outlier detection and removal
  - Multicollinearity Resolution: Addressed high correlations between male/female population totals  

- **Statistical Analysis Framework**
  - Distribution Assessment: Shapiro-Wilk tests confirmed non-normal distributions (p < 0.05)
  - Correlation Analysis: Multicollinearity assessment and relationship mapping between variables  

- **Inferential Statistics**
  - Kruskal-Wallis tests for comparing variables across risk categories
  - Chi-square tests for categorical variable associations
  - Mann-Whitney U tests for continuous variable relationships  

- **Regression Modeling**
  - Linear Regression: Predicting COVID-19 deaths using socioeconomic and demographic predictors
  - Logistic Regression: Classifying health risk categories ("Above Average", "High Risk", etc.)
  - Model Validation: Residual analysis, Cook's Distance, and diagnostic plotting
  - Performance Metrics: R-squared, accuracy, sensitivity, specificity, and confidence intervals  

- **Visualization and EDA**
  - Distribution Analysis: Histograms revealing pandemic impact variations across counties
  - Relationship Mapping: Scatter plots showing poverty-case correlations
  - Geographic Patterns: State-level analysis of population, poverty, and demographic distributions
  - Risk Stratification: Bar charts displaying county risk category distributions  

- **Key Statistical Results**
  - Age: Significant association with depression severity (p<0.001)
  - Income: Higher income protective — counties with >$150K income had better outcomes
  - Poverty Rate: Strongest positive predictor of COVID-19 deaths
  - Health Risk Index: Negative relationship (better risk management = lower fatalities)  

- **Model Performance Comparison**

  | Model              | Accuracy / R² | Performance Area   |
  |--------------------|---------------|--------------------|
  | Linear Regression  | R² = 0.85     | Death prediction   |
  | Logistic Regression| 98.53%        | Risk classification|

## Clinical Applications

  - **Targeted Resource Allocation**: Prioritize high-poverty counties for pandemic preparedness  
- **Health Equity Initiatives**: Address underlying socioeconomic factors affecting vulnerability  
- **Community-Based Interventions**: Develop culturally appropriate prevention programs for minority communities  
- **Risk Stratification Tools**: Use predictive models for early identification of vulnerable counties  
- **Policy Development**: Evidence-based approaches for equitable healthcare resource distribution  

## Limitations

- **Removal of Outliers**: Eliminating outliers might reduce variability and overlook extreme cases.  
- **Correlation, Not Causation**: The study shows correlations, not causality. For example, poverty is linked to higher COVID-19 cases and deaths, but it doesn't prove a direct cause-and-effect relationship.  
- **Data Distribution Assumptions**: While non-parametric tests are robust for non-normal data, they are less sensitive than parametric tests, potentially limiting the detection of small but meaningful differences.  


## Future Research Directions
Future research should focus on longitudinal studies tracking pandemic impacts over time, intervention studies testing targeted support strategies for high-risk communities, and expanding analysis to include biological markers and healthcare infrastructure variables. Cross-cultural validation across diverse healthcare systems will improve generalizability, while implementation science approaches are needed to translate findings into effective public health policies and pandemic preparedness strategies.

## Contributors

- **Aakriti Bhandari**
- **Sai Sathvik Appagana**
- **Sai Srilekha Aluri**
- **Sri Jahnavi Adusumilli**

## Contact

For questions or suggestions, please contact:  
Sri Jahnavi Adusumilli - [srijadus@iu.edu](mailto:srijadus@iu.edu)
