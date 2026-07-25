# Does Digital Orientation Drive ESG Performance?
A Cross-Sector Analysis of Indian Listed Companies (NIFTY 500, FY2023-24)
---
This study examines whether a company's Digital Orientation (DO) measured across four dimensions adapted from Kindermann et al. (2021), significantly predicts its Environmental, Social and Governance (ESG) performance among Nifty 500 companies for fiscal year 2023-24.
Using Computer-Aided Text Analysis (CATA) applied to annual reports and CRISIL ESG ratings, the analysis covers 437 companies with both valid DO Scores and ESG Ratings.

#Research Questions
---
Primary Research Question (PRQ)
---
Does digital orientation (measured across 4 dimensions) significantly predict ESG performance among Nifty 500 companies, after controlling for industry effects?

Secondary Research Questions (SRQ)
---
Q1: Which of the four digital orientation dimensions is most strongly associated with ESG performance?
Q2: Does the DO-ESG relationship vary significantly across sectors?
Q3: Are there companies with high digital orientation but low ESG performance (or vice versa), and what industries do they cluster in?

# Dataset 
---
| Metric       | DO Score | ESG Rating |
| ------------ | -------- | ---------- |
| **N**        | 487      | 444        |
| **Mean**     | 6.344    | 57.858     |
| **Median**   | 5.084    | 58.000     |
| **Std. Dev** | 4.958    | 5.841      |
| **Min**      | 0.128    | 41         |
| **Max**      | 30.792   | 77         |
---
**Primary Analysis Sample**: 437 firms with both DO Score and ESG Rating.
**Industries Covered**: 21 distinct NSE sectoral classifications including Information Technology, Financial Services, Capital Goods, Chemicals, Metals & Mining, and more.

# Methodology
---
Digital Orientation Score Construction
Adapted from Kindermann et al. (2021), European Management Journal. The construct measures four dimensions via keyword frequency analysis in FY2023-24 annual reports:

| Dimension                              | Description                                    |
| -------------------------------------- | ---------------------------------------------- |
| **Digital Technology Scope**           | Breadth of technologies mentioned              |
| **Digital Capabilities**               | Human capital and skills investments           |
| **Digital Ecosystem Coordination**     | Partnerships and platform orientation          |
| **Digital Architecture Configuration** | IT infrastructure, cybersecurity, data systems |

Normalization: 
DO Score = (Sum of 4 sub-scores / Total words in report) × 1000
---
Segmentation: Tertile splits based on 33rd (3.83) and 67th (6.44) percentiles:
Low DO: < 3.83
Medium DO: 3.83 – 6.44
High DO: > 6.44

**ESG Data**
---
Source: CRISIL ESG Ratings (India's leading credit rating agency)
Scale: 0–100 (higher = better ESG performance)
Categories: Leadership, Strong, Adequate, Below Average

Analytical Methods
---
Descriptive Analysis & Distribution Characteristics

Pearson & Spearman Correlations (full sample + industry-stratified)

One-Way ANOVA with Tukey HSD Post-hoc Tests

OLS Regression: Three nested models

Model 1 (Baseline): Unadjusted DO -> ESG

Model 2 (Industry FE): DO -> ESG + Industry Fixed Effects

Model 3 (Sub-score Decomposition): Four dimensions -> ESG + Industry FE

Divergence Quadrant Analysis: Median-split classification

# Key Results
---
1. Primary Finding: No Independent DO-ESG Relationship
   
| Model                     | DO Coefficient | p-value       | R²        | Interpretation        |
| ------------------------- | -------------- | ------------- | --------- | --------------------- |
| **Model 1 (Baseline)**    | β = 0.145      | **p = 0.010** | 0.015     | Small but significant |
| **Model 2 (Industry FE)** | β = 0.043      | p = 0.353     | **0.434** | **Not significant**   |

Once industry fixed effects are introduced, the DO coefficient shrinks by ~70% and loses all statistical significance. Industry membership alone explains 43.4% of variance, a 28-fold increase over the unadjusted model.

2. Only One Dimension Matters: Architecture Configuration
   
| Dimension                              | Coefficient     | p-value    | Significant? |
| -------------------------------------- | --------------- | ---------- | ------------ |
| Digital Technology Scope               | β = -0.0052     | 0.277      | No           |
| Digital Capabilities                   | β = +0.0026     | 0.321      | No            |
| Digital Ecosystem Coordination         | β = -0.0074     | 0.116      | No            |
| **Digital Architecture Configuration** | **β = +0.0032** | **0.0008** | **Yes**    |

**Insight**: Infrastructure-specific investment (IT systems, cybersecurity, data governance) is the only dimension with an independent, industry-adjusted association with ESG.

3. Sectoral Heterogeneity: Only Capital Goods Shows Significance
   
| Industry                     | Pearson r  | p-value   | Significant? |
| ---------------------------- | ---------- | --------- | ------------ |
| **Capital Goods**            | **+0.384** | **0.005** | **Yes**    |
| Construction                 | +0.543     | 0.068     | Marginally   |
| Automobile & Auto Components | +0.340     | 0.077     | Marginally   |
| Information Technology       | -0.023     | 0.916     | No           |
| Financial Services           | +0.036     | 0.742     | No            |
| Metals & Mining              | -0.308     | 0.245     | No            |

**Surprise**: Information Technology — the most digitally intensive sector — shows zero correlation (r = -0.023, p = 0.916), likely due to ceiling effects and digital orientation being "table stakes."

4. Divergence Analysis: High Digital / Low ESG
   
Quadrant Distribution (Median Splits):
| Quadrant              | N      | %         | Description              |
| --------------------- | ------ | --------- | ------------------------ |
| High DO / High ESG    | 146    | 33.4%     | Aligned Positive         |
| Low DO / Low ESG      | 134    | 30.7%     | Aligned Negative         |
| Low DO / High ESG     | 84     | 19.2%     | ESG Leaders (no digital) |
| **High DO / Low ESG** | **73** | **16.7%** | **Divergence**        |

**Critical Finding*: High Digital / Low ESG companies cluster in Chemicals (10) and Capital Goods (10) — not in Financial Services and IT as hypothesized. This suggests digital tools in manufacturing do not automatically translate to sustainability outcomes.


#Limitations
---
Measurement: DO Scores are keyword-count based they measure what companies say about digital technology in annual reports, not necessarily what they do operationally.
Data: Single year snapshot (FY2023-24); single ESG provider (CRISIL); 14 companies lack DO scores, 57 lack ESG ratings.
Methodology: OLS assumes linearity; industry fixed effects control for average sector differences but not firm-level confounders (size, profitability, ownership structure).
Generalizability: Findings are specific to the Indian regulatory context (BRSR) and may not generalize to other emerging or developed markets.



