# Student Performance Analysis using Statistical Learning Theory

This repository contains the code for a statistical learning theory project focused on understanding the multifaceted factors that influence student academic performance and success.

## Project Objective

The primary objective of this project is to investigate the relationships between various student and parental attributes—including socioeconomic indicators (e.g., parental occupation categories) and student academic choices (e.g., course selection priorities and prior grades)—and their ultimate academic outcomes, such as course completion and graduation. The study employs advanced statistical learning techniques to uncover patterns and dependencies within educational data.

## Methodology

This project utilizes a data-driven approach, incorporating key steps:
* **Data Preprocessing:** Cleaning and preparing raw student performance data.
* **Feature Engineering:** Creating relevant features, such as `final_grade` from semester grades.
* **One-Hot Encoding:** Converting categorical variables like student `Target` (Dropout, Enrolled, Graduate) into a numerical format suitable for machine learning models using `OneHotEncoder` from `sklearn.preprocessing`.
* **Outlier Detection:** Identifying and handling anomalies within the dataset using techniques like Isolation Forest (`IsolationForest` from `sklearn.ensemble`) to ensure robust model performance.
* **Statistical Modeling:** Applying statistical learning theory methods to analyze the influence of different variables on student success metrics. The project utilized Python libraries such as `matplotlib.pyplot` and `seaborn` for data visualization, `math` for mathematical functions, `scipy.stats` (e.g., `stats.t.interval`, `stats.f_oneway`, `zscore`, `norm`, `chi2`, `f`, `t`, `ttest_ind`) for statistical functions and hypothesis testing, `numpy` (e.g., `np.std`, `np.percentile`) for numerical computations, and `statsmodels.stats.power` (e.g., `zt_ind_solve_power`) for test power analysis.

## Dataset

The analysis is based on a comprehensive dataset that includes various student demographics, academic records (e.g., curricular units, grades, evaluations), and parental information (e.g., qualifications, occupations, age at enrollment).

## Key Findings & Conclusion

The project report, "Statistical Learning Theory Project Report," explored the initial hypothesis concerning whether students from parents in occupational categories traditionally associated with higher socioeconomic status might face challenges in courses they chose with lowest priorities and had poor previous grades, impacting their success in passing courses and graduating. The study utilized a combined approach of quantitative analysis of academic performance data with qualitative insights from the dataset.

**Primary Finding:** The findings indicated no significant correlation between parents' social status and their children's academic outcomes, suggesting that students from higher-status backgrounds did not experience challenges in their studies as initially hypothesized. Despite having chosen courses with lower priority and having weaker past academic performance, their results were similar to other students, with comparable chances of successfully completing courses and graduating.

**Visual Analysis:**
* **Target State Comparison:** Visual comparisons of "Target" states (Graduate, Enrolled, Dropout) between the hypothesized group and all students revealed that the hypothesized group had a higher percentage of graduates (23.2% vs. 18.4% for all students) and fewer dropouts (46.5% vs. 50.4% for all students) compared to the overall student body.
* **Ridge Plot Analysis:** Ridge plots illustrating the distribution of final grades across different academic outcomes for socially prominent students (calculated from the final average of the first and second semester averages ) showed:
    * For `Target_Dropout`, a higher dropout rate was observed at lower final grades, indicating a strong negative relationship between final grade and dropout rate.
    * For `Target_Enrolled`, there were significant distributions around grades 10 and higher, suggesting a weak or no relationship between final grade and enrollment rate, implying that students with similar grades might have different enrollment statuses.
    * For `Target_Graduate`, a large peak was observed around final grades of 13-14, indicating a strong positive relationship between final grade and graduation rate.

**Statistical Test Results:**
* One-Sample t-tests and z-tests were conducted, and the null hypothesis (that there is no impact on course completion and graduation against children of parents with higher prestige, power, or income) could not be rejected, providing no evidence to support the initial hypothesis of challenges.
* A significant limitation noted was the low statistical power of the test. It was determined that 3748 samples were required for robust conclusions, whereas the total dataset had less than 2000 samples, potentially impacting the findings.
* Tests for equality of variances between the groups (children of high prestige parents and children of lower prestige parents) also showed no significant differences.

**Correlation Analysis:**
* A correlation heatmap revealed relationships between various features. For graduation, factors such as second-semester grade, final average, updated tuition fees, and selection priority showed a positive correlation. For dropout, factors like age at enrollment, gender, and debt showed a positive correlation.
* A regression formula for `Target_Dropout` and `Age at enrollment` was obtained as `Y = -0.4X + 21.3`.

**Overall Conclusion:** The project concluded that parental background was not a sufficient predictor for the educational outcomes of their student children, and no notable challenges were found. However, the report suggests that if the sample size were sufficiently large, the results might differ. The research emphasizes the importance of addressing inequalities and providing equal opportunities and support mechanisms to promote fair and inclusive educational environments for all students, regardless of their parents' socioeconomic status.

## Technologies Used

* Python
* Pandas (for data manipulation)
* Numpy (for numerical operations)
* Scikit-learn (for machine learning models)
* Matplotlib (for data visualization)
* Seaborn (for statistical data visualization)
* SciPy (for statistical functions)
* Statsmodels (for statistical modeling and power analysis)
