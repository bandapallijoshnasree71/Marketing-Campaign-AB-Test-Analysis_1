# Marketing Campaign A/B Test Analysis

A statistical inference and experimentation project developed to evaluate whether a new website landing page improves conversion rates compared with an existing landing page. The project uses Python-based hypothesis testing, confidence interval analysis, and statistical power analysis to assess experimental outcomes and support data-driven marketing decisions.

## Business Objective

Determine whether a newly designed website landing page increases user conversion rates compared with the existing landing page, evaluate the statistical significance of the observed difference, quantify conversion impact, and provide a data-driven recommendation to support marketing optimization decisions.

## Experiment Groups

### 1. Control Group (Existing Landing Page)

Represents users exposed to the existing landing page and establishes the baseline conversion rate used to evaluate the performance of the newly designed landing page.

### 2. Treatment Group (New Landing Page)

Represents users exposed to the newly designed landing page. The experiment evaluates whether the redesigned page improves conversion behavior compared with the control group.

## Exploratory Data Analysis

Analyzed user-level experiment data to examine experiment group distribution, conversion outcomes, landing page assignment consistency, and experimental data quality.

- Total Users Analyzed: 266,508
- Control Group Users: 133,264
- Treatment Group Users: 133,244
- Control Group Conversions: 16,067
- Treatment Group Conversions: 15,813
- Control Conversion Rate: 12.06%
- Treatment Conversion Rate: 11.87%

## Experiment Results

| Metric | Control | Treatment |
| :--- | :---: | :---: |
| **Total Users** | 133,264 | 133,244 |
| **Total Conversions** | 16,067 | 15,813 |
| **Conversion Rate** | 12.06% | 11.87% |

### Conversion Rate Comparison

Evaluated the conversion performance of the control and treatment groups to measure the observed effectiveness of the new landing page.

- **Control Conversion Rate**: 12.06%
- **Treatment Conversion Rate**: 11.87%
- **Absolute Difference**: -0.1888 percentage points
- **Relative Lift**: -1.57%

The treatment group recorded a lower observed conversion rate compared with the control group. Statistical testing was conducted to determine whether the observed difference provides evidence of a conversion improvement.


## Statistical Hypothesis Testing

A one-sided Two-Proportion Z-Test was conducted to evaluate whether the new landing page significantly improves conversion rates compared with the existing landing page.

### Hypothesis Formulation

- **Null Hypothesis (H₀)**: The new landing page does not improve conversion rates compared with the existing landing page.
- **Alternative Hypothesis (H₁)**: The new landing page improves conversion rates compared with the existing landing page.

### Test Configuration

- **Statistical Test**: Two-Proportion Z-Test
- **Test Direction**: One-Sided
- **Significance Level (α)**: 0.05
- **Confidence Level**: 95%
- **Alternative Hypothesis Direction**: Treatment conversion rate greater than control conversion rate

### Statistical Results

| Metric | Result |
| :--- | :---: |
| **Z-statistic** | -1.5019 |
| **P-value** | 0.933434 |
| **Significance Level** | 0.05 |
| **Absolute Difference** | -0.1888 percentage points |
| **Relative Lift** | -1.57% |

The p-value exceeds the selected significance level of 0.05. Therefore, the null hypothesis is not rejected. The experiment does not provide sufficient statistical evidence that the new landing page improves conversion rates.

## Confidence Interval Analysis

Calculated a 95% confidence interval for the difference in conversion rates between the treatment and control groups to quantify uncertainty surrounding the observed experiment effect.

- **Absolute Difference**: -0.1888 percentage points
- **Lower Bound**: -0.4352 percentage points
- **Upper Bound**: +0.0576 percentage points
- **95% Confidence Interval**: [-0.4352, +0.0576] percentage points

The confidence interval includes zero, indicating that the experiment does not establish a statistically significant difference in conversion rates. The results are compatible with a small positive improvement, no difference, or a decline in conversion rates.
## Power Analysis

A statistical power analysis was conducted to estimate the sample size required to detect a 1 percentage-point absolute improvement in conversion rate from the baseline conversion rate of 12.06% to a target conversion rate of 13.06%.

### Power Analysis Configuration

- **Baseline Conversion Rate**: 12.06%
- **Target Conversion Rate**: 13.06%
- **Target Absolute Improvement**: 1 percentage point
- **Statistical Power**: 80%
- **Significance Level**: 5%
- **Allocation Ratio**: 1:1
- **Test Direction**: One-Sided

### Power Analysis Results

| Metric | Result |
| :--- | :---: |
| **Effect Size (Cohen's h)** | 0.03018 |
| **Required Sample Size per Group** | 13,572 |
| **Total Required Sample Size** | 27,144 |

The power analysis estimates that approximately 13,572 users per group would be required to detect the predefined 1 percentage-point absolute improvement under the selected statistical assumptions.

## Statistical Significance vs. Practical Significance

Statistical significance evaluates whether the experimental evidence is sufficient to reject the null hypothesis, whereas practical significance considers whether the magnitude of the observed effect is meaningful enough to justify a business decision.

- **Statistical Outcome**: No statistically significant evidence of conversion improvement
- **Observed Absolute Difference**: -0.1888 percentage points
- **Observed Relative Lift**: -1.57%
- **95% Confidence Interval**: Includes zero

The experiment did not demonstrate a statistically significant improvement in conversion rates. Business decisions should also consider implementation costs, potential revenue impact, customer experience, and other marketing objectives.

## Business Recommendation

### DON'T SHIP

The new landing page achieved an observed conversion rate of 11.87%, compared with 12.06% for the existing landing page.

The one-sided hypothesis test did not provide sufficient statistical evidence that the new landing page improves conversion rates. The 95% confidence interval also includes zero.

The recommendation is to retain the existing landing page and avoid deploying the new version based on conversion improvement alone. Further experimentation or redesign may be considered to identify opportunities for conversion optimization.

## Project Workflow

1. Imported and explored the experiment dataset using Pandas
2. Examined dataset dimensions, data types, column names, and statistical summaries
3. Identified missing values, duplicate records, duplicate user assignments, and experiment data inconsistencies
4. Validated experiment group and landing page assignment consistency
5. Conducted Exploratory Data Analysis to examine user distribution and conversion outcomes
6. Calculated conversion counts, conversion rates, absolute difference, and relative lift
7. Formulated null and alternative hypotheses for the experiment
8. Conducted a one-sided Two-Proportion Z-Test using Statsmodels
9. Calculated 95% confidence intervals to evaluate uncertainty around conversion rate differences
10. Performed statistical power analysis to estimate sample size requirements for a predefined conversion improvement
11. Evaluated statistical significance and practical significance
12. Developed a business recommendation based on statistical findings
13. Prepared an executive summary to communicate experiment outcomes and business implications

## Tools and Skills

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Google Colab
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Statistical Inference
- Hypothesis Testing
- Two-Proportion Z-Test
- Confidence Interval Analysis
- Statistical Power Analysis
- Conversion Rate Optimization
- Business Insights
- Data-Driven Decision-Making

## Project Files

- `Marketing_Campaign_AB_Test_Analysis.ipynb` — Complete Python analysis, statistical testing, and visualizations
- `ab_data.csv` — Experiment dataset
- `executive_summary.md` — Business-oriented experiment summary and recommendation

## Project Status

Completed — Data cleaning, exploratory data analysis, conversion rate comparison, hypothesis testing, confidence interval analysis, power analysis, and final business recommendation implemented using Python in Google Colab.
