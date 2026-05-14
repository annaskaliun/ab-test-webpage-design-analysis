# A/B Test Analysis: New Webpage Design Performance

## Business Problem

The company tested a new webpage design and needed to determine whether it improves user behavior compared to the existing version.

The key business question:

**Should the new webpage design be rolled out to all users?**

The analysis compares the control group, which saw the old design, with the treatment group, which saw the new design.

---

## Project Objective

Evaluate the impact of the new webpage design on:

- Conversion rate
- Average session duration
- Average number of pages visited
- Performance across age groups

The goal was to determine whether the observed differences between the control and treatment groups were statistically significant and relevant for business decision-making.

---

## Dataset

The dataset contains user-level A/B test results.

| Column | Description |
|---|---|
| `user_id` | Unique user identifier |
| `variant` | Test group: control or treatment |
| `converted` | Conversion flag: 1 if the user converted, 0 otherwise |
| `session_duration` | Session duration in minutes |
| `pages_visited` | Number of pages visited |
| `age` | User age |

---

## Methodology

The analysis included:

1. Data quality check
2. Calculation of key metrics by variant
3. Statistical testing
4. Age group segmentation
5. Tableau dashboard creation
6. Business recommendation

Statistical tests used:

| Metric | Test |
|---|---|
| Conversion rate | Two-proportion z-test |
| Average session duration | t-test |
| Average pages visited | t-test |

Significance level:

alpha = 0.05

## Key Results
Metric	Control	Treatment	Difference
Users	5,013	4,987	-
Conversions	534	715	+181
Conversion Rate	10.65%	14.34%	+3.69 p.p.
Average Session Duration	5.03 min	7.02 min	+1.99 min
Average Pages Visited	2.98 pages	5.01 pages	+2.03 pages

The treatment group outperformed the control group across all key metrics.

Statistical Test Results
Metric	Test	Statistic	p-value	Result
Conversion Rate	Two-proportion z-test	-5.57	2.50e-08	Significant
Average Session Duration	t-test	-44.37	0.00	Significant
Average Pages Visited	t-test	-51.29	0.00	Significant

All tested metrics showed statistically significant differences between the control and treatment groups.

Age Group Analysis
Age Group	Control CR	Treatment CR	Result
<25	9.89%	14.69%	Treatment higher
25–34	11.31%	13.32%	Treatment higher
35–44	10.33%	15.48%	Treatment higher
45+	10.75%	14.17%	Treatment higher

The new design improved conversion rate across all age groups.
The strongest conversion performance was observed in the 35–44 age group.

## Business Insights
Conversion rate increased from 10.65% to 14.34%
Absolute conversion uplift was +3.69 percentage points
Relative conversion uplift was approximately +34.6%
Average session duration increased by +1.99 minutes
Average pages visited increased by +2.03 pages
Treatment performed better across all age groups
Statistical testing confirmed that the differences were significant
Recommendation

The new webpage design should be rolled out to all users.

The treatment version delivered higher conversion, longer session duration, and more page views. Since all key differences were statistically significant, the new design can be considered a better-performing version.

After rollout, conversion and engagement metrics should continue to be monitored, especially across age groups.

## Dashboard
(https://public.tableau.com/app/profile/hanna.skaliun/viz/ab2_17784192086600/ABTestDashboardNewWebpageDesignPerformance)

The Tableau dashboard includes:

Control vs treatment KPI cards
Conversion rate by variant
Average session duration
Average pages visited
Statistical test results
Performance by age group 

## Tools Used
Python (Pandas, NumPy, SciPy, Statsmodels)
Tableau
Jupyter Notebook
