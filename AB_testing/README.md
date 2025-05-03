
# 🧪 A/B Testing: Sample Size & Experiment Simulation

This project explores two fundamental steps for conducting a proper A/B test:

1. **Estimating the Required Sample Size (`AB_testing_sample_size.ipynb`)**
2. **Simulating and Evaluating A/B Test Results (`AB_testing_experiment.ipynb`)**

---

## 📊 Objective

To provide an interactive and didactic workflow for understanding how sample size affects the outcome of A/B experiments and how different statistical tests behave when testing null hypotheses.

---

## 📁 Notebooks

### 1. `AB_testing_sample_size.ipynb` – Sample Size Estimation

This notebook calculates the **minimum number of users** required to detect a specific lift (expected increase in conversion rate) with a desired confidence level and statistical power.

#### ⚙️ Customizable Parameters:
- `baseline_conversion`: base conversion rate (e.g., 0.1 = 10%)
- `expected_lift`: expected increase in conversion rate (e.g., 0.01 = 1%)
- `exposure_rate`: percentage of users exposed to the test (treatment) group
- `alpha`: significance level (probability of Type I error)
- `power`: statistical power (1 - probability of Type II error)

#### 📈 Observations:

- The **smaller the expected lift**, the **larger the sample size** required to detect it.
- **Lower alpha values** (e.g., 0.01) increase the required sample size substantially.
- **Low exposure rates** (e.g., only 5% of users in the test group) significantly increase the total sample size needed.

---

### 2. `AB_testing_experiment.ipynb` – A/B Experiment Simulation

Using the sample size calculated previously, this notebook simulates A/B experiments under different scenarios:

- **No difference** between control and test groups
- **Small lift** (e.g., +1%)
- **Large lift** (e.g., +10%)

Each experiment is analyzed using the following statistical tests:

#### 🧪 Applied Statistical Tests

- **Shapiro-Wilk Test**: Tests for normality. Important to decide whether parametric tests are appropriate.
- **Z-Test for Proportions**: Checks for differences in proportions (e.g., conversion rates) between groups.
- **T-Test (Independent Samples)**: Parametric test comparing means when normality is assumed.
- **Mann-Whitney U Test**: Non-parametric test comparing medians; robust to non-normal data.
- **Bayesian Inference**: Estimates the probability distribution of the conversion difference; provides interpretable results like "X% probability that variant B is better than A".

#### 📊 Key Findings:

- When there's **no real lift**, tests **generally fail to reject the null hypothesis**, as expected.
- With a **1% lift**, test outcomes vary — showing the difficulty of detecting small effects, especially with smaller samples.
- With a **10% lift**, all tests clearly **reject the null**, confirming a true positive effect.

Bar charts illustrate the conversion rates for each scenario, helping visualize the performance difference (or lack thereof).

---

## 📦 Requirements

The notebooks were developed in **Google Colab** using:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

from scipy.stats import shapiro, ttest_ind, mannwhitneyu, norm
from statsmodels.stats.proportion import proportions_ztest, proportion_effectsize
from statsmodels.stats.power import NormalIndPower
```

---

## 📘 How to Use

1. Open the notebooks in Google Colab.
2. Customize your experiment parameters.
3. Use `AB_testing_sample_size` to compute the necessary sample size.
4. Plug these values into `AB_testing_experiment` to simulate outcomes and evaluate test results.

---

## 📌 Conclusion

This project demonstrates that setting an appropriate sample size is **critical** to achieving reliable A/B test results. It also illustrates how different statistical methods behave depending on the effect size, data distribution, and sample allocation.

Whether you're testing small tweaks or major changes, using the right tools and planning ahead can drastically improve the trustworthiness of your experiment outcomes.

## 📎 Connect with Me

If you found this project useful or want to collaborate, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/nathanferig/).

