# Independent Samples t-Test – Titanic Fare Analysis

## 📊 Project Overview

This project demonstrates the application of an **Independent Samples t-Test** to determine whether there is a statistically significant difference in the average fare paid by male and female passengers in the Titanic dataset.

The analysis was performed using Python, Pandas, NumPy, SciPy, Matplotlib, Seaborn, and Google Colab/Jupyter Notebook.

---

## 🎯 Objective

The primary objective of this project is to statistically evaluate whether two independent groups differ in their average values.

In this project, the average **Titanic fare** paid by male and female passengers is compared using an independent samples Welch's t-test.

---

## ❓ Research Question

> Is there a statistically significant difference between the average fare paid by male and female Titanic passengers?

---

## 📁 Dataset

The project uses the **Titanic dataset**, which contains information about passengers who travelled on the Titanic.

The important variables used in this analysis are:

| Variable | Description |
|----------|-------------|
| `sex` | Passenger's sex |
| `fare` | Passenger's ticket fare |

### Groups

- **Female passengers**
- **Male passengers**

### Dependent Variable

- `fare`

### Independent/Grouping Variable

- `sex`

---

## 🧪 Hypothesis Formulation

### Null Hypothesis (H₀)

There is no statistically significant difference between the average fare paid by male and female passengers.

**H₀: μ₁ = μ₂**

### Alternative Hypothesis (H₁)

There is a statistically significant difference between the average fare paid by male and female passengers.

**H₁: μ₁ ≠ μ₂**

### Significance Level

The significance level used for the hypothesis test is:

**α = 0.05**

---

## 🔬 Methodology

The following steps were performed:

1. Imported the required Python libraries.
2. Loaded the Titanic dataset.
3. Inspected the structure and characteristics of the dataset.
4. Selected the `sex` and `fare` variables.
5. Checked for missing values.
6. Removed observations with missing values.
7. Divided the data into male and female passenger groups.
8. Calculated descriptive statistics for both groups.
9. Visualized fare distributions using box plots and histograms.
10. Performed Welch's Independent Samples t-Test.
11. Calculated the mean difference.
12. Calculated a 95% confidence interval.
13. Calculated Cohen's d effect size.
14. Compared the p-value with the significance level.
15. Interpreted the statistical result.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **SciPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab / Jupyter Notebook**

---

## 📌 Statistical Test

A **Welch Independent Samples t-Test** was used.

Welch's t-test was selected because it does not require the two groups to have equal population variances.

The test was performed using SciPy's `ttest_ind()` function with:

```python
stats.ttest_ind(
    male_fare,
    female_fare,
    equal_var=False,
    alternative='two-sided'
)


📈 Results
The following results were obtained:
Metric
Result
t-statistic
-5.0775
p-value
0.000001
Mean Difference (Female − Male)
18.9559
Cohen's d
0.3877
Significance Level
0.05
📊 Interpretation
The obtained p-value was:
p = 0.000001
The significance level was:
α = 0.05
Since:
p < α
or
0.000001 < 0.05
the null hypothesis is rejected.
Therefore, there is statistically significant evidence of a difference in the average fare paid by male and female Titanic passengers.
The mean difference was approximately 18.96, indicating that female passengers paid a higher average fare than male passengers in this dataset.
The Cohen's d value was 0.3877, indicating a small-to-moderate effect size.
📉 Visualizations
The project includes visualizations such as:
1. Fare Distribution by Sex
A box plot was used to compare the distribution of fares between male and female passengers.
2. Fare Distribution Histogram
A histogram with KDE was used to inspect the distribution of fares for the two groups.
3. Average Fare Comparison
A bar chart was used to compare the average fare between male and female passengers.
🔍 Key Findings
The average fare differs between male and female passengers.
The Welch independent samples t-test produced a p-value of 0.000001.
The result is statistically significant at the 5% significance level.
The null hypothesis was rejected.
Female passengers had a higher average fare in this dataset.
The Cohen's d effect size of 0.3877 indicates a small-to-moderate difference.
The fare variable shows considerable variation and contains high-value observations.
✅ Final Conclusion
The analysis provides statistically significant evidence that the average fare paid by male and female Titanic passengers was different.
Since the p-value was significantly smaller than 0.05, the null hypothesis was rejected.
The analysis demonstrates how an Independent Samples t-Test can be used to determine whether an observed difference between two independent groups is statistically significant.
However, statistical significance does not necessarily imply a large practical effect. The Cohen's d value of 0.3877 suggests that the magnitude of the difference is relatively small to moderate.
📂 Project Structure
independent-samples-ttest/
│
├── independent_samples_ttest_titanic.ipynb
├── README.md
├── requirements.txt
│
├── images/
│   ├── fare_boxplot.png
│   ├── fare_distribution.png
│   └── average_fare.png
│
└── results/
    └── statistical_results.txt

💡 Learning Outcomes
Through this project, I learned:
How independent samples t-tests work.
How to formulate statistical hypotheses.
How to compare two independent groups.
How to calculate and interpret a p-value.
How to interpret a t-statistic.
How to use Welch's t-test.
How to inspect distributions before statistical testing.
How to calculate confidence intervals.
How to calculate and interpret Cohen's d.
How to communicate statistical findings using visualizations.
