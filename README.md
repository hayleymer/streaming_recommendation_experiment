# Streaming Recommendation Engine Experiment Analysis

## Business Problem

Streaming platforms rely heavily on recommendation systems to increase user engagement, retention, and advertising revenue. Even small improvements in engagement can have significant commercial impact at scale.

However, measuring the true impact of a new recommendation algorithm requires careful experimental design and statistical validation. Observed differences in engagement may be driven by demographic imbalance or sampling bias rather than the algorithm itself.

This project evaluates whether a new recommendation engine increases average daily viewing hours compared to the existing system, while also assessing the integrity and validity of the experimental design.

The objective is to determine whether observed engagement differences can be attributed to the recommendation engine rather than structural differences between user groups.

---

## Dataset

The dataset contains subscriber-level data from an A/B test experiment, including:

- User demographic information  
- Engagement behaviour metrics  
- Treatment and control group assignment  
- Daily viewing hours  

### Key variables used

Primary outcome variable:

- Hours_Watched_Per_Day  

Treatment indicator:

- Group (A = Control, B = Treatment)

User characteristics:

- Age  
- Gender  
- Demographic group  
- Months active on platform  
- Social metric (prior engagement indicator)

The experiment began on 18 July, and only post-intervention observations were included in the analysis. :contentReference[oaicite:1]{index=1}

---

## Approach

### Data Preparation

- Loaded and cleaned subscriber-level data  
- Filtered dataset to include only post-intervention observations  
- Renamed variables for clarity and consistency  
- Verified group assignments and data integrity  

### Exploratory Data Analysis

Exploratory analysis was conducted to understand relationships between user characteristics and engagement.

Key analyses included:

- Pairwise variable relationships using scatterplot matrices  
- Visualisation of engagement patterns across demographic groups  
- Exploration of relationships between engagement and age, demographic group, and prior engagement  

These analyses provided initial insight into potential drivers of engagement.

### Regression Analysis

Linear regression models were used to evaluate relationships between engagement and user characteristics, including:

- Age  
- Demographic group  
- Prior engagement (social metric)

Model diagnostics were performed to evaluate regression assumptions including linearity and residual distribution.

### Experimental Integrity and Bias Assessment

Group composition was analysed to identify potential sampling bias.

Key findings included:

- Significant gender imbalance between treatment and control groups  
- Male-to-female ratio in treatment group was substantially higher than in control group  
- Differences in demographic subgroup distribution between groups  

These imbalances introduce potential confounding effects that weaken causal interpretation.

### Statistical Testing and Power Analysis

Statistical testing was conducted to evaluate treatment effects:

- Two-sample t-tests comparing treatment and control groups  
- Effect size calculation across demographic subgroups  
- Power analysis to assess sample adequacy  
- Variance and normality testing  

These analyses evaluated whether observed differences were statistically significant and practically meaningful.

---

## Results

The treatment group demonstrated modestly higher average daily viewing hours compared to the control group.

Key findings:

- Treatment group showed increased engagement on average  
- Effect sizes varied across demographic subgroups  
- Some differences reached statistical significance  

However, structural imbalance between treatment and control groups limits the ability to attribute engagement differences solely to the recommendation engine.

Demographic imbalance introduces confounding effects that weaken causal conclusions.

---

## Key Findings

The analysis revealed several critical insights:

- The new recommendation engine may improve engagement  

<img width="1750" height="1081" alt="difference_viewing_hours" src="https://github.com/user-attachments/assets/9f05d612-90d1-493b-8b89-b168064cc0a4" />

- Demographic imbalance between treatment and control groups introduces bias  
- Gender and demographic composition differed significantly between groups  
- Structural imbalance weakens causal interpretation of observed differences

This demonstrates the importance of experimental design integrity in evaluating algorithm performance.

Without balanced randomisation, observed treatment effects may reflect underlying group differences rather than true algorithm impact.

---

## Tech Stack

R  
dplyr  
ggplot2  
readr  
lubridate  
pwr  

### Analytical Techniques

- Exploratory data analysis  
- Linear regression modelling  
- Experimental bias assessment  
- Statistical hypothesis testing  
- Effect size estimation  
- Power analysis  
- Experimental design evaluation  

---

## How to Run

### Clone repository

```bash
git clone https://github.com/hayleymer/streaming-recommendation-experiment.git
```

### Navigate to project folder

```bash
cd streaming-recommendation-experiment
```

### Install required R packages

```r
install.packages(c("dplyr", "ggplot2", "readr", "lubridate", "pwr"))
```

Run the R Markdown file to reproduce the full experimental analysis.
