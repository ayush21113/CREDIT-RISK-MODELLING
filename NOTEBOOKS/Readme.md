# Credit Risk Case Study

This project involves data preprocessing, feature selection, and statistical analysis for credit risk modeling

- Loaded two datasets: `case_study1.xlsx` and `case_study2.xlsx` using `pandas.read_excel()`.
- Created deep copies of the data for further processing.

## 2. Data Cleaning
- Removed rows with placeholder values like `-99999` from key columns.
- Dropped columns from `df2` with more than 10,000 invalid entries.

## 3. Data Merging
- Merged the two datasets using an inner join on `PROSPECTID` to ensure no null values remain.

## 4. Categorical Feature Inspection
- Identified categorical columns based on their data types.

## 5. Chi-Square Test
- Performed the Chi-Square test between selected categorical variables and the target variable `Approved_Flag` to evaluate statistical independence.

## 6. Variance Inflation Factor (VIF) Check
- Calculated VIF scores for all numerical features.
- Retained only those features with VIF less than or equal to 6 to reduce multicollinearity.

## 7. ANOVA Test
- Conducted an ANOVA (Analysis of Variance) test for the retained numerical variables.
- Retained only features with a p-value less than or equal to 0.05, indicating statistically significant differences among groups in the target variable.

## 8. Final Selected Features
A total of 39 features were selected after applying the VIF and ANOVA tests. These features are intended to be used for subsequent model training and evaluation.


