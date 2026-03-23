# Netflix Content Strategy Analysis — Python EDA Portfolio Project

https://colab.research.google.com/drive/15zLsHVC4wt9QdI4DE6e_aqt01AVM_pHe?usp=sharing

## Executive Summary

This project delivers a comprehensive Exploratory Data Analysis (EDA) of Netflix's global content library using Python. Moving beyond surface-level visualization, this analysis replicates the content strategy intelligence framework used by media analytics teams at leading streaming platforms — interrogating genre saturation, market-specific rating distributions, strategic content shifts, and release timing optimization across 8,807 titles spanning 2008–2021.

---

## Business Objectives

- Determine whether Netflix is strategically pivoting from Movies toward TV Shows for higher subscriber retention
- Identify oversaturated vs underserved genre categories to surface content investment gaps
- Assess whether specific markets receive disproportionately mature content — a key indicator of localization strategy
- Pinpoint optimal content release windows to understand Netflix's go-to-market timing playbook

---

## Dataset

| Attribute | Detail |
|---|---|
| Source | Netflix Movies and TV Shows — Kaggle |
| Records | 8,807 titles |
| Features | 12 variables |
| Domain | Media & Entertainment Analytics |
| Period | 2008 – 2021 |

Key fields: `type`, `title`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`

---

## Technical Environment

- **Language:** Python 3
- **Libraries:** Pandas, Matplotlib, Seaborn
- **Platform:** Google Colab
- **Skills Demonstrated:** Data cleaning, missing value treatment, datetime parsing, groupby aggregations, data visualization, business insight generation

---

## Data Cleaning Summary

Before analysis, the dataset required structured cleaning across multiple dimensions:

| Issue | Column | Action Taken |
|---|---|---|
| 2,634 missing values | `director` | Filled with 'Unknown' |
| 825 missing values | `cast` | Filled with 'Unknown' |
| 831 missing values | `country` | Filled with 'Unknown' |
| 4 missing values | `rating` | Filled with 'Not Rated' |
| 10 missing values | `date_added` | Retained as NaT |
| Wrong data type | `date_added` | Converted to datetime |

Post-cleaning, `year_added` and `month_added` were engineered as new features from `date_added` to enable time-series analysis.

---

## Exploratory Analysis

### Overview Visualizations

**1. Movies vs TV Shows Distribution**
Netflix's library skews heavily toward Movies (6,131) vs TV Shows (2,676) — a 70/30 split that sets the baseline for strategic shift analysis.

**2. Top 10 Content-Producing Countries**
The United States dominates with 2,800+ titles. India ranks second at ~950, followed by the United Kingdom at ~420 — reflecting Netflix's aggressive international content investment strategy.

**3. Content Growth Over Time**
Netflix's library grew exponentially from near-zero in 2015 to a peak of 2,000+ titles added in 2019, followed by a post-COVID contraction in 2020–2021 — a visible inflection point in content acquisition strategy.

---

## Business Analysis & Findings

---

### BQ1 — Is Netflix Shifting Strategy from Movies to TV Shows?
**Analyst Hypothesis:** Netflix may be pivoting toward TV Shows for higher engagement and subscriber retention.

![Strategic Shift Chart](Screenshot%202026-03-23%20130142.png)

**Finding:** Movies consistently dominate but the gap is narrowing. TV Shows grew from 26 titles added in 2015 to 505 in 2021, while Movies grew from 56 to 993. The Movies-to-TV Shows ratio compressed from 2.2x in 2015 to 2.0x in 2021 — a gradual but measurable strategic pivot toward serialized content.

---

### BQ2 — Genre Saturation Analysis: Where Are the Content Gaps?
**Analyst Hypothesis:** A few genres dominate the library while niche categories remain systematically underserved.

![Genre Saturation Chart](Screenshot%202026-03-23%20130338.png)

**Finding:** International Movies (2,752), Dramas (2,427), and Comedies (1,674) are severely oversaturated. Meanwhile, Docuseries (395) and Kids' TV (451) represent significantly underserved categories — representing white space opportunities for content investment with lower competitive density and potentially higher marginal viewer acquisition value.

---

### BQ3 — Content Rating by Market: Are Some Countries Getting More Mature Content?
**Analyst Hypothesis:** Netflix may be deploying market-specific content rating strategies based on cultural and regulatory factors.

![Rating by Country Chart](Screenshot%202026-03-23%20130824.png)

**Finding:** The United States receives the most mature content by volume — TV-MA titles dominate the US library at 900+ titles. India's library skews toward TV-14 (550+), reflecting regulatory content sensitivity. South Korea and Japan show minimal mature content, consistent with stricter local broadcasting standards. This confirms Netflix operates a deliberate market-specific content rating strategy rather than a uniform global approach.

---

### BQ4 — Release Timing Optimization: When Does Netflix Drop Most Content?
**Analyst Hypothesis:** Netflix concentrates content releases in strategic windows to maximize subscriber acquisition and retention.

![Release Month Chart](Screenshot%202026-03-23%20131004.png)

**Finding:** July is Netflix's peak content release month (827 titles) — aligning with summer viewing season and subscriber growth targets. December ranks second (813), consistent with holiday engagement strategy. February is the lowest volume month (563) — suggesting Netflix deliberately deprioritizes post-holiday periods when subscriber churn risk is lower. This data supports a bimodal release calendar: summer peak and holiday peak.

---

## Key Strategic Recommendations

**1. Invest in Underserved Genres** — Docuseries and Kids' TV show the lowest content density relative to audience demand. Incremental investment in these categories offers higher differentiation value than adding to already-saturated Drama or Comedy pipelines.

**2. Accelerate the TV Show Pivot** — The narrowing Movies-to-TV Shows ratio reflects a deliberate strategy. Given TV Shows' superior engagement and retention metrics industry-wide, accelerating this pivot would strengthen Netflix's competitive moat against Disney+ and HBO Max.

**3. Optimize Release Calendar** — With July and December confirmed as peak release windows, marketing and content acquisition teams should align budget deployment to these months to maximize new title visibility and subscriber acquisition efficiency.

---

## Skills Demonstrated

| Skill | Applied In |
|---|---|
| Data loading & inspection | Cell 1 |
| Missing value analysis | Cell 2 |
| Data cleaning & feature engineering | Cell 3 |
| Bar & line chart visualization | Viz 1, 2, 3 |
| Time-series trend analysis | BQ1 |
| Text parsing & explode() | BQ2 |
| Multi-variable groupby analysis | BQ3 |
| Conditional color formatting | BQ4 |

---

## About

Developed as part of a data analytics portfolio targeting business intelligence, media analytics, and content strategy roles. The analytical framework mirrors the content performance intelligence approach used by strategy and analytics teams at global streaming platforms.

**Author:** Himani Garg
**LinkedIn:** [linkedin.com/in/himani-garg-0a94571b2](https://www.linkedin.com/in/himani-garg-0a94571b2/)
**Tools:** Python 3, Pandas, Matplotlib, Google Colab, GitHub
**Dataset:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
