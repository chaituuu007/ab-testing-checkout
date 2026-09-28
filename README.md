# 🧪 A/B Testing — Checkout Conversion Experiment

> Statistical analysis of a website checkout A/B experiment to determine whether a new checkout experience produces a statistically significant improvement in conversion rate.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![Statistics](https://img.shields.io/badge/Statistics-A%2FB%20Testing-purple)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 📌 Project Overview

This project analyzes a synthetic website checkout experiment in which visitors were randomly assigned to two groups:

- **Control (A):** Existing checkout experience
- **Variant (B):** New checkout experience

The objective is to determine whether Variant B produces a statistically significant improvement in checkout conversion.

The analysis uses statistical hypothesis testing, confidence intervals, and effect-size calculations to support an evidence-based business decision.

---

## 🎯 Business Objective

The business wants to determine whether the redesigned checkout experience should replace the existing checkout.

The analysis answers:

- What is the conversion rate for Control A?
- What is the conversion rate for Variant B?
- How large is the observed conversion lift?
- Is the difference statistically significant?
- What is the 95% confidence interval?
- Should the business treat Variant B as a validated improvement?

---

## 🧪 Experiment Design

### Control Group — A

Visitors experience the existing checkout process.

### Variant Group — B

Visitors experience the redesigned checkout process.

The primary metric is:

**Checkout Conversion Rate**

\[
Conversion\ Rate = \frac{Conversions}{Visitors}
\]

---

## 📊 Dataset

The experiment contains visitor-level observations with treatment assignment and conversion outcome.

### Main variables

| Variable | Description |
|---|---|
| `visitor_id` | Unique visitor identifier |
| `group` | Control or Variant |
| `converted` | Whether the visitor completed checkout |

The dataset is synthetic and is intended for analytics/statistics demonstration.

---

## 🧹 Data Preparation

The analysis included:

- Loading the visitor-level experiment data
- Checking dataset structure
- Validating treatment groups
- Checking conversion values
- Separating Control and Variant groups
- Calculating sample sizes
- Calculating conversion counts and rates

---

## 📐 Hypothesis Testing

### Null Hypothesis — H₀

There is no difference in conversion rates between Control A and Variant B.

\[
H_0: p_B = p_A
\]

### Alternative Hypothesis — H₁

The conversion rates between Control A and Variant B are different.

\[
H_1: p_B \neq p_A
\]

### Significance Level

\[
\alpha = 0.05
\]

A two-sample proportion Z-test was used to evaluate the difference.

---

## 📈 Experiment Results

| Metric | Control A | Variant B |
|---|---:|---:|
| Visitors | 600 | 600 |
| Conversions | 57 | 71 |
| Conversion Rate | 9.50% | 11.83% |

### Conversion Lift

**Absolute lift:**

**+2.33 percentage points**

**Relative lift:**

**+24.56%**

Variant B produced a higher observed conversion rate in this experiment.

---

## 📊 Statistical Results

| Statistical Metric | Result |
|---|---:|
| Z-statistic | 1.3092 |
| P-value | 0.1905 |
| Chi-square statistic | 1.7141 |
| Chi-square p-value | 0.1905 |
| Significance level | 0.05 |
| 95% CI for B − A | -1.16% to +5.82% |

---

## 🔍 Interpretation

The observed conversion rate increased from **9.50%** in Control A to **11.83%** in Variant B.

However, the statistical test produced a **p-value of 0.1905**, which is greater than the 0.05 significance threshold.

Therefore, the observed difference is **not statistically significant at the 5% level**.

The 95% confidence interval for the conversion-rate difference ranges from approximately **-1.16 percentage points to +5.82 percentage points**, which includes zero.

This means the experiment does not provide sufficient statistical evidence to establish that Variant B produces a reliable conversion improvement.

---

## 💼 Executive Decision

### Decision: Retain Control A for now

Variant B showed a promising observed conversion increase, but the experiment did not reach statistical significance.

Therefore, Variant B should **not be treated as a statistically validated improvement based on this experiment alone**.

A business could consider collecting additional observations and running another appropriately designed experiment before making a permanent rollout decision.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **SciPy**
- **Matplotlib**
- **Statistical Hypothesis Testing**
- **A/B Testing**
- **Two-Proportion Z-Test**
- **Chi-Square Test**
- **Confidence Intervals**
- **Effect Size Analysis**

---

## 📁 Project Structure

```text
ab-testing-checkout/
│
├── README.md
├── AB_Test_Report.pdf
├── checkout_ab_test_analysis.ipynb
├── checkout_ab_test_cleaned.csv
└── checkout_ab_test_v2.csv
