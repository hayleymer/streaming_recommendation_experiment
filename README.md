# Business Impact Evaluation: Streaming Recommendation Engine Experiment

This project evaluates the commercial impact of a revised streaming recommendation engine using experimental A/B test data.

## Business Objective

Assess whether the updated recommendation algorithm (Group B) increased average daily viewing hours compared to the existing system (Group A), while evaluating the integrity of the experimental design.

## Analytical Approach

The analysis includes:

- Data preparation and post-intervention filtering
- Exploratory data analysis
- Linear and multiple regression modelling
- Model diagnostics and assumption testing
- Experimental integrity and bias assessment
- Subgroup treatment effect evaluation
- Effect size calculation
- Statistical power analysis

## Key Insight

The treatment group demonstrated modest increases in average viewing hours. However, demographic imbalance between experimental groups limits the strength of causal attribution.

## Recommendation

Before full deployment, a follow-up experiment using stratified randomisation is recommended to ensure balanced demographic representation and stronger causal inference.

## Repository Contents

- `ab_test_recommendation_engine.Rmd` — Full analytical workflow
- `ab_test_recommendation_engine.html` — Rendered business report

## Requirements

R version 4.0+

Required packages:

- dplyr
- ggplot2
- readr
- lubridate
- pwr
- GGally
