# County-Level Unemployment and Rurality Analysis

A linear regression project examining whether county rurality predicts unemployment rates, and how that relationship changes when educational attainment and median household income are controlled for.

## Research Question

Does a county's Rural-Urban Continuum Code predict its unemployment rate, and does that relationship hold once education and income are accounted for?

## Data Sources

- **Unemployment and Median Household Income** : USDA Economic Research Service, County-level Data Sets
- **Educational Attainment (1970–2023)** : USDA Economic Research Service, County-level Data Sets

Both datasets were merged on FIPS county code, resulting in a final analytic sample of 3,134 U.S. counties.

## Methods

Data cleaning and analysis were performed in R using the tidyverse (dplyr, readr, tidyr, ggplot2). Three nested linear regression models were estimated:

1. **Model 1** : Unemployment rate regressed on rurality alone
2. **Model 2** : Adds educational attainment and median household income
3. **Model 3** : Log-transformed unemployment rate, estimated after diagnostic testing revealed heteroskedasticity and non-normal residuals in Models 1 and 2

## Key Finding

Rurality alone appears to predict *higher* unemployment (Model 1), but this relationship reverses once education and income are controlled for (Models 2–3) : more rural counties show modestly *lower* unemployment than urban counties with comparable education and income levels. This is consistent with omitted variable bias in the simple bivariate model.

## Files

- `Project1_Rfile_test.Rmd` : R Markdown source: data cleaning, merging, descriptive statistics, regression models, and diagnostics
- `Project1_Rfile_test.pdf` : Knitted output with full code, results, and plots

## Author

Chelsea Oliveira
