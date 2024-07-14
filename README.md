
# College Success Predictors: A Machine Learning Approach

## Project Overview

This project applies machine learning techniques to understand educational outcomes using the College Scorecard data from the U.S. Department of Education. The primary objective is to identify university-level factors that predict strong retention and graduation rates. The project explores various data features related to financial metrics, institutional characteristics, and student demographics to provide insights into higher education success metrics.
I have written a blogpost on Medium on this work. Please find it here - https://medium.com/@justinesylivera/uncovering-the-secrets-of-student-success-a-machine-learning-journey-6c89336220a3

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Descriptive Analysis](#descriptive-analysis)
- [Exploratory and Predictive Analysis](#exploratory-and-predictive-analysis)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributors](#contributors)
- [License](#license)

## Installation

To run this project, you need to have Python installed on your system along with the required libraries. You can install the necessary libraries using the following command:

```bash
pip install -r requirements.txt
```

## Dataset

The dataset used in this project is the College Scorecard data provided by the U.S. Department of Education. It contains comprehensive information about U.S. colleges and universities, including attributes such as tuition costs, graduation rates, student demographics, and more.

## Descriptive Analysis

### Descriptive Questions:
1. **What are the average retention and graduation rates across different institutions?**
   - Summary statistics and box plots are used to understand central tendencies and variability.
2. **What are the distributions of tuition fees, student demographics, and financial aid among the institutions?**
   - Histograms are used to provide an overview.
3. **How do retention and graduation rates vary by institution type (e.g., public vs. private, four-year vs. less-than-four-year institutions)?**
   - Box plots are used to explore potential differences.
4. **How do financial factors (e.g., tuition fees, student loan amounts) relate to retention and graduation rates?**
   - Scatter plots are used to understand the impact.
5. **How do student demographics (e.g., gender, race/ethnicity, socioeconomic background) influence retention and graduation rates?**
   - Scatter plots are used to investigate the potential impact.
6. **What are the relationships between different variables?**
   - A correlation matrix is used to analyze the relationships.

## Exploratory and Predictive Analysis

### Exploratory Questions:
1. **Which financial factors most significantly impact student loan default rates at universities?**
   - Box plots and scatter plots are used to explore relationships.
2. **How do student demographics correlate with post-graduation salaries?**
   - Scatter plots and correlation matrices are used to analyze correlations.

### Predictive Questions:
1. **What university-level factors predict strong retention and graduation rates?**
   - Machine learning models are used to predict these outcomes.

## Data Preprocessing

### Steps:
1. **Load the Dataset**: Import the dataset and load it into a pandas DataFrame.
2. **Check for Missing Values**: Identify and handle missing values.
3. **Convert Data Types**: Ensure all columns have the correct data types.
4. **Impute Missing Values**: Use appropriate imputation techniques to fill in missing values.
5. **Feature Selection**: Select relevant features for the analysis.
6. **Data Splitting**: Split the data into training and testing sets.

### Variables Used:
- **Financial Features**: TUITIONFEE_IN, TUITIONFEE_OUT, AVGFACSAL, DEBT_MDN, PCTPELL, COSTT4_A, COSTT4_P, NPT4_PUB, NPT4_PRIV, PCTFLOAN.
- **Institutional Features**: CONTROL, REGION, LOCALE, ADM_RATE, SAT_AVG, ACTCMMID, UGDS, C150_4, RET_FT4, RET_PT4.
- **Student Demographic Features**: UGDS_WHITE, UGDS_BLACK, UGDS_HISP, UGDS_ASIAN, AGE_ENTRY, FEMALE, FIRST_GEN, DEP_STAT_PCT_IND, PELL_EVER, FAMINC, MD_FAMINC, PAR_ED_PCT_1STGEN.
- **Other Features**: UG25abv, PFTFAC, C150_L4, RET_FT_L4, RET_PT_L4, AVGFACSAL, NPT41_PUB, NPT41_PRIV, FTFTPCT, COSTT4_PUB, COSTT4_PRIV, DEBT_N, FAMINC_IND, SATVR25, SATVR75, SATMT25, SATMT75, PAR_ED_PCT_MS.

## Modeling

The following models were used to predict retention and graduation rates:

1. **LightGBM**: A gradient boosting framework that uses tree-based learning algorithms.

### Training the Models:

The models were trained using the selected features. Categorical features were handled appropriately by converting them to the category dtype.

## Evaluation

The models were evaluated using the following metrics:

1. **Mean Absolute Error (MAE)**: The average magnitude of errors in predictions.
2. **Mean Squared Error (MSE)**: The average squared difference between actual and predicted values.
3. **R-squared (R²)**: Indicates the proportion of variance in the dependent variable that is predictable from the independent variables.

### Results Interpretation:

Feature importance was analyzed to identify the most significant predictors for retention and graduation rates. The top 10 features by importance were plotted for both models.

## Results

The analysis identified several key factors that influence retention and graduation rates. The models achieved good predictive performance, and the feature importance analysis provided valuable insights into which factors are most impactful.

### Top 10 Features for Retention Rate:
1. **RET_FT4_POOLED**: Retention rate of full-time students.
2. **UG25ABV**: Percentage of undergraduates aged 25 and above.
3. **UGDS**: Undergraduate student enrollment.
4. **DEP_STAT_PCT_IND**: Percentage of independent students.
5. **AGE_ENTRY**: Average age of entry for students.
6. **PFTFAC**: Percentage of full-time faculty.
7. **AVGFACSAL**: Average faculty salary.
8. **C150_4**: Graduation rate within 150% of expected time for 4-year programs.
9. **DEBT_N**: Number of students with debt.
10. **PCTFLOAN**: Percentage of students receiving federal loans.

### Top 10 Features for Graduation Rate:
1. **C150_4**: Graduation rate within 150% of expected time for 4-year programs.
2. **PCTPELL**: Percentage of students receiving Pell grants.
3. **RET_PT4_POOLED**: Retention rate of part-time students.
4. **RET_FT4_POOLED**: Retention rate of full-time students.
5. **ADM_RATE**: Admission rate.
6. **AGE_ENTRY**: Average age of entry for students.
7. **PFTFAC**: Percentage of full-time faculty.
8. **AVGFACSAL**: Average faculty salary.
9. **FEMALE**: Percentage of female students.
10. **DEBT_MDN**: Median debt of graduates.

## Contributors

- Your Name (Project Lead)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

### Additional Files

- `requirements.txt`: Contains the list of required Python
