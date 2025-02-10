# Was-a-Website-Redesign-Successful?

## Table of Contents
1. [Introduction](#1-introduction)
2. [Objectives](#2-objectives)
3. [Executive Summary](#3-executive-summary)
4. [Methodology](#4-methodology)
5. [Insights](#5-insights)
6. [Recommendations](#6-recommendations)
7. [Conclusion](#7-conclusion)
8. [Future Studies](#8-future-studies)
9. [Limitations of the Study](#9-limitations-of-the-study)

---

### 1. Introduction
Optimizing user engagement on a website is critical for business success. For startups, understanding the impact of design changes on user behavior can significantly influence growth strategies. This study evaluates the effect of a redesigned landing page on user conversion rates. Using data collected from an A/B test, we assess whether the new design had a statistically significant impact on conversions.

Key variables include:
- **`treatment`**: Whether the user was exposed to the new design (`yes`) or the old design (`no`).
- **`new_images`**: Whether new images were used on the landing page (`yes` or `no`).
- **`converted`**: Whether the user converted (`1`) or not (`0`).

---

### 2. Objectives
This analysis aims to:
1. Determine if the redesigned landing page (`treatment = yes`) significantly increases the conversion rate compared to the original design.
2. Assess whether the presence of new images (`new_images = yes`) affects conversion rates.
3. Provide actionable insights and recommendations based on the findings.

---

### 3. Executive Summary
Our analysis found that the redesigned landing page led to a statistically significant increase in conversions (p-value = 0.025). However, the presence of new images did not significantly impact conversions (p-value = 0.888). Logistic regression further confirmed these findings, with the odds ratio for the treatment group being 1.073, indicating a modest improvement in conversion likelihood.

The results suggest the new design should be implemented platform-wide. Further research could explore other factors influencing conversion rates to optimize the user experience.

---

### 4. Methodology
The following approach was used:

1. **Data Exploration**:
   - Summary statistics of conversion rates across combinations of `treatment` and `new_images`.
   - A balance check to ensure `new_images` did not confound the results.

2. **Statistical Testing**:
   - Two-sample proportion test comparing conversion rates between the treatment and control groups.
   - Logistic regression to control for the potential influence of `new_images`.

3. **Interpretation**:
   - Interpretation of statistical results to evaluate the redesigned landing page's effectiveness.

---

### 5. Insights

#### 1. Summary Statistics:
| Treatment | New Images | Converted Rate |
|-----------|------------|----------------|
| no        | no         | 0.107104       |
| no        | yes        | 0.112538       |
| yes       | no         | 0.120047       |
| yes       | yes        | 0.113724       |

- Overall conversion rates:
  - Control (`treatment = no`): 0.109821
  - Treatment (`treatment = yes`): 0.1168855

#### 2. Balance Check:
| Treatment | New Images | Proportion |
|-----------|------------|------------|
| no        | no         | 0.5        |
| no        | yes        | 0.5        |
| yes       | no         | 0.5        |
| yes       | yes        | 0.5        |

- Since `new_images` is balanced, it does not confound the results.

#### 3. Two-Sample Proportion Test:
- **Z-statistic**: -2.242
- **P-value**: 0.025
- **Conclusion**: The difference in conversion rates is statistically significant.

#### 4. Logistic Regression:
| Variable           | Coefficient | Std Err | Z-value | P>|z| | Odds Ratio |
|--------------------|-------------|---------|---------|------|------------|
| Intercept          | -2.0904     | 0.027   | -76.314 | 0.000 | N/A        |
| Treatment_yes      | 0.0703      | 0.031   | 2.242   | 0.025 | 1.073      |
| New_images_yes     | -0.0044     | 0.031   | -0.141  | 0.888 | 0.996      |

- The treatment group has a significant positive effect on conversion rates, with an odds ratio of 1.073, meaning users exposed to the new design are 7.3% more likely to convert.
- New images do not significantly affect conversions.

---

### 6. Recommendations
1. **Implement the Redesigned Landing Page**:
   - The new design improves conversions and should be deployed platform-wide.

2. **Focus on Other Design Elements**:
   - Consider testing other design elements (e.g., layout, color schemes) to further optimize performance.

3. **Monitor Post-Implementation Performance**:
   - Track conversion rates after implementation to ensure sustained improvements.

4. **Conduct Further Experiments**:
   - Explore additional factors like user demographics and device types to enhance understanding.

---

### 7. Conclusion
The redesigned landing page led to a significant increase in user conversion rates. However, the addition of new images did not yield meaningful improvements. These insights can help the business enhance its user acquisition strategy.

---

### 8. Future Studies
1. **Segmentation Analysis**:
   - Investigate conversion rates across user segments (e.g., age, location).

2. **Longitudinal Impact**:
   - Study the long-term effects of the redesign on user retention.

3. **Multivariate Testing**:
   - Test multiple design elements simultaneously to identify impactful changes.

4. **Machine Learning Models**:
   - Leverage advanced models to predict conversion probabilities and improve the user journey.

---

### 9. Limitations of the Study
1. **Sample Size and Duration**:
   - Limited sample size and study duration may impact generalizability.

2. **External Factors**:
   - External variables like seasonality or competitor activity were not accounted for.

3. **Confounding Variables**:
   - Other unobserved factors may influence the results, despite balancing `new_images`.
