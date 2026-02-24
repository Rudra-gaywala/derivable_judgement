# Derivable Judgement: Statistical Decision-Making Model

## Project Overview
This project is a statistical analysis tool designed to apply inferential statistics to a synthetic health dataset. It generates a dataset of health records (including age, BMI, smoking status, and disease indicators) and performs various hypothesis testing techniques to derive judgments about significant factors affecting disease occurrence.

The analysis is performed using Python, leveraging libraries such as Pandas, NumPy, and SciPy for calculation, and follows a structured approach to hypothesis testing.

## Technologies Used
* **Python 3.x**
* **Pandas:** Data manipulation and analysis.
* **NumPy:** Numerical computing and data generation.
* **SciPy (stats):** Scientific computing for T-tests, Chi-Square, ANOVA, and other statistical functions.

## Dataset Structure
The project includes a module to generate a synthetic dataset (`health_data.csv`) with the following fields:

| Field Name | Data Type | Description |
| :--- | :--- | :--- |
| `age` | Int | Age of the individual |
| `age_group` | String | Categorical group (e.g., "18-25", "60+") |
| `gender` | String | Male, Female, Other |
| `region` | String | Geographic region (North, South, East, West) |
| `smoking_status`| String | Smoker, Non-Smoker, Former Smoker |
| `weight` | Float | Weight in kg |
| `bmi` | Float | Body Mass Index |
| `glucose_level` | Float | Blood glucose level (mg/dL) |
| `cholesterol` | Float | Total cholesterol level (mg/dL) |
| `diabetes` | Binary | 0 (No) or 1 (Yes) |

## Analysis & Operations Performed

The project performs the following statistical tasks as outlined in the "Derivable Judgement" assignment:

### 1. Data Generation
* Simulates a dataset of 1,000 health records.
* Implements logic to correlate BMI with weight and Glucose with Age to ensure realistic statistical testing results.

### 2. Hypothesis Formulation
* Establishes Null ($H_0$) and Alternative ($H_1$) hypotheses for T-tests (Smoking effects), Chi-Square (Region vs. Disease), and ANOVA (Age vs. Glucose).

### 3. Confidence Intervals
* Calculates the 95% Confidence Interval (CI) for key numerical variables such as **Age** and **Weight** to estimate the population mean.

### 4. T-Test Analysis
* Performs an **Independent Two-Sample T-Test**.
* Compares the mean BMI of "Smokers" versus "Non-Smokers".
* Calculates the **T-statistic** and **Critical Value** to determine significance.

### 5. Chi-Square Test of Independence
* Conducts a Chi-Square test on categorical variables (**Region** vs. **Diabetes**).
* Generates a contingency table of observed frequencies.
* Computes the Chi-Square statistic and p-value to test for dependency.

### 6. Analysis of Variance (ANOVA)
* Performs a **One-Way ANOVA** test.
* Compares the mean Glucose Levels across five different **Age Groups**.
* Determines if there is a statistically significant difference between at least one pair of groups.

### 7. Covariance and Correlation
* Computes a **Covariance Matrix** to determine the direction of relationships between continuous variables.
* Computes a **Correlation Matrix** (Pearson coefficient) to measure the strength of relationships between **Age**, **BMI**, **Glucose**, and **Weight**.

### 8. Statistical Interpretation
* Each test block outputs the calculated **p-value** and compares it against a significance level ($\alpha = 0.05$).
* The code automatically prints a decision to either **"Reject $H_0$"** or **"Accept $H_0$"** based on the results.

## License
This project is for educational purposes under the "Derivable Judgement" skill education module.
