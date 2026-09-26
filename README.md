# COVID-19 Mortality Analysis in R

## 📌 Project Overview

This project uses **R** to analyse a COVID-19 line-list dataset and investigate factors associated with COVID-19 mortality.

The analysis focuses on:

- Overall COVID-19 death rate
- Age differences between people who died and those who survived
- Gender differences in COVID-19 mortality
- Statistical significance using two-sample t-tests
- Descriptive statistics using the `Hmisc` package

## 🛠️ Tools and Technologies

- R
- RStudio
- Hmisc
- Statistical hypothesis testing
- CSV data

## 📊 Dataset

The project uses a COVID-19 line-list CSV dataset containing individual-level COVID-19 records.

The R script imports the dataset using `read.csv()` and uses `Hmisc::describe()` to produce descriptive statistics.

## 🔍 Analysis Performed

### 1. Data Preparation

A binary `death_dummy` variable is created from the original death column:

- `1` = died
- `0` = did not die

The overall death rate is then calculated.

### 2. Age Analysis

The dataset is divided into:

- People who died
- People who did not die

The mean age of each group is calculated.

A two-sample t-test is then used to determine whether the difference in age is statistically significant.

### 3. Gender Analysis

Male and female records are separated and the mean death rate is calculated for each group.

A two-sample t-test is used to test whether the difference between the groups is statistically significant.

The analysis reports:

- Male death rate: approximately 8.5%
- Female death rate: approximately 3.7%
- p-value: 0.002

Because the p-value is less than 0.05, the result is statistically significant.

## 📈 Statistical Interpretation

For hypothesis testing:

> **If p-value < 0.05, we reject the null hypothesis.**

For the gender comparison, the p-value is **0.002**, which is less than 0.05.

Therefore:

> **The result is statistically significant and the null hypothesis is rejected.**

The script also reports a **99% confidence interval**, indicating that the estimated difference in mortality between men and women is approximately **0.8% to 8.8%**.

## 📁 Project Structure

```text
COVID19-R-Mortality-Analysis/
│
├── COVID19_line_list_data.csv
├── script_covid_r.R
└── README.md# COVID19-R-Mortality-Analysis
COVID-19 mortality analysis using R, including descriptive statistics, age and gender comparisons, and statistical hypothesis testing.
