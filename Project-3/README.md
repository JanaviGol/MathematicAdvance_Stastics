# 📊 Part A: Theoretical Foundation

Welcome to the theoretical foundation of the **Derivable Judgement** project. This section provides a comprehensive guide from basic statistical concepts to advanced hypothesis testing methods used in data science.

---

## 📈 1. Inferential Statistics
* **What is it?** Inferential statistics is a branch of statistics used to make predictions, generalizations, or decisions about a large group (called the **Population**) based on data collected from a smaller group (called the **Sample**).
* **Why do we use it?** In the real world, it is almost impossible or too expensive to collect health data from every single person in a country. Therefore, we take a representative sample of 170 individuals and use inferential statistics to draw conclusions about the whole society.
* **Key Concept:** It connects sample findings to population truths using probability theory.

---

## 🎯 2. Hypothesis Testing and its Components
* **What is it?** Hypothesis testing is a formal step-by-step statistical method used to test whether a claim or assumption about a dataset is true or not.
* **Core Components:**
    1.  **Null Hypothesis (H0):** The status quo or the assumption of "no effect," "no difference," or "no relationship." For example: *Smoking has no effect on Diabetes.*
    2.  **Alternative Hypothesis (H1 or Ha):** The claim we want to prove. It states that there is a significant effect, difference, or relationship. For example: *Smoking significantly affects Diabetes.*
* **The Logic:** We always start by assuming H0 is true. We only reject H0 if our sample data provides overwhelming evidence against it.

---

## 📏 3. Confidence Interval and Critical Value
* **Confidence Interval (CI):** * It is a range of values (e.g., between 49 and 55 years old) derived from sample data that is highly likely to contain the true population parameter.
    * A **95% Confidence Interval** means that if we repeat the study 100 times, 95 times the calculated interval will contain the true population average.
* **Critical Value:** * It is a threshold or cutoff value determined from standard statistical tables (like Z-table or T-table) based on our chosen significance level (usually alpha = 0.05).
    * If our calculated test statistic falls beyond this critical value, it enters the **Rejection Region**, and we reject the Null Hypothesis.

---

## 🔢 4. p-value (Probability Value)
* **What is it?** The p-value is the probability of obtaining test results at least as extreme as the results observed during the test, assuming that the Null Hypothesis (H0) is completely true.
* **Decision Rules:**
    * **If p-value alpha (0.05):** The result is statistically significant. We **Reject H0** and accept H1.
    * **If p-value alpha (0.05):** The result is not significant. We **Fail to Reject H0** (Accept H0).
* **Golden Rule:** *"If the p-value is low, the Null must go. If the p-value is high, the Null will fly."*

---

## ⚠️ 5. Type I and Type II Errors
Statistical tests are based on probabilities, which means there is always a small chance of making an incorrect decision.

| Error Type | Common Name | What Actually Happens | Real-World Impact Example |
| :--- | :--- | :--- | :--- |
| **❌ Type I Error** | False Positive | We reject a **true** Null Hypothesis (H0). | Telling a healthy patient they have diabetes when they do not. |
| **⚠️ Type II Error** | False Negative | We fail to reject a **false** Null Hypothesis (H0). | Telling a sick patient they are perfectly healthy when they actually have diabetes. |

* **Significance Level (alpha):** The probability of committing a Type I error, controlled by the analyst (usually set to 5%).

---

## 🧪 6. Statistical Tests (When to use what?)

### 🔹 A. z-test
* **Usage:** Compares the means of two groups.
* **Conditions:** Used when the sample size is large (n > 30) and the population standard deviation (sigma) is known.

### 🔹 B. t-test
* **Usage:** Compares the means of two groups (e.g., comparing the average BMI of Males vs. Females).
* **Conditions:** Used when the sample size is small (n < 30) or when the population standard deviation is unknown (which is true for most real-world datasets).

### 🔹 C. Chi-Square Test (chi^2)
* **Usage:** Tests the relationship or association between two **Categorical** variables (e.g., checking if `smoking_status` is independent of `diabetes`).
* **Output:** Tells you if the distribution of categories happens by random chance or due to a real underlying connection.

### 🔹 D. ANOVA Test (Analysis of Variance)
* **Usage:** Compares the means of **three or more** independent groups (e.g., comparing the average glucose levels across multiple `age_groups` like 18-25, 26-35, 46-60, and 60+).
* **Why not multiple t-tests?** Running multiple t-tests increases the chance of making a Type I error. ANOVA checks all groups simultaneously.

---

## 🔄 7. Covariance vs. Correlation

Both terms measure the relationship between two continuous numerical variables (like `age` and `bmi`), but they have distinct differences:

### 📉 Covariance
* **Definition:** Measures how two variables change together.
* **Direction Only:** * **Positive Covariance:** If variable A increases, variable B tends to increase.
    * **Negative Covariance:** If variable A increases, variable B tends to decrease.
* **Limitation:** The scale depends entirely on the units of the data (e.g., kg, cm), so you cannot compare the covariance of age/weight with height/blood pressure easily.

### 🔗 Correlation (Pearson's $r$)
* **Definition:** A standardized version of covariance that measures both the **direction** and the **strength** of a linear relationship.
* **Fixed Scale:** The value always ranges strictly from **-1.0 to +1.0**.
    * **+1.0**: Perfect positive linear relationship.
    * **0.0**: No linear relationship at all.
    * **-1.0**: Perfect negative linear relationship.
* **Advantage:** It is unitless, making it perfect for comparing any two variables regardless of their measurement scales.