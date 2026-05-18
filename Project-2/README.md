##### **📊 Student Performance \& Probability Analysis Report**



A comprehensive data-driven study utilizing probability theory to analyze factors influencing student final exam performance. This analysis evaluates student datasets using empirical results, theoretical baselines, random variables, conditional logic, and Bayesian updating.





**🛠️ 1. Setup \& Environment**



The analysis is powered by the following core Python libraries for data manipulation, statistical computing, and visualization:



**Dataset:** expectation\_decider\_dataset.csv (Tracks student metrics such as study\_ hours, attendance, group\_ discussion, and final\_ exam\_ pass).





**🎲 2. Core Probability Event Foundations**



We categorize our statistical observations into two primary types of probabilities based on the dataset attributes.



**Empirical Probability (Experimental):**



Calculated directly from the real-world historical outcomes observed within the project dataset.



**Target Event:** Student passing the final exam.



Formula Applied:



###### &#x20;                  **Empirical Probability = Students Passed\\Total Registered Students**



**🧠 Theoretical Probability**



Determined by mathematical reasoning and baseline assumptions, assuming perfectly balanced, equally likely outcomes.



**Target Event:** Participation in Group Discussions (Binary Choice: Yes or No).



Formula Applied:



###### &#x20;              **Theoretical Probability = 1\\Total Possible Outcomes= {1}\\{2} = 0.5**





**📈 3. Random Variables \& Binomial Distributions**



To project performance trends across small groups of students, we model passing outcomes using a discrete random variable distributed binomially.



🔢 Variable Definition (X)



Let X be the random variable representing the number of successful exam passes out of a trial sample size n.



**Sample Size (n):** 3 students 

**Probability of Success (p):** 0.645 (Derived from dataset passing rate)

**Sample Space (x values):** {0, 1, 2, 3}



**📉 Probability Distribution Table** 



Computed using the Binomial Probability Mass Function (PMF): P(X = x) = bi nom{n}{x} p ^ x (1-p)^{n-x}



**Property Verification:** sum P(X = x) = 1.0 (The sum of all outcomes equals total certainty).



**📏 Expected Values \& Spread**



Mean / Expected Value E(X): The long-run average outcome expected from multiple sample selections.E(X) = n times p = 3 times 0.645 = 1.935 Variance 

Var(X): The measure of data spread around the computed mean value.Var(X) = n times p times (1 - p) = 3 times 0.645 times 0.355 = 0.687





**🟢 4. Venn Diagram (Overlapping Habits)**



This section visualizes the relationship between two important student habits:



**Set A:** Students with Study Hours > 10 hours (only\_ A)

**Set B:** Students with Attendance > 80% (only\_ B)



Intersection (A cap B): Students meeting both conditions (both)



We use the matplotlib Venn library to plot these segments and see how many students balance both habits.





**📋 5. Contingency Tables \& Joint Analytics**



By creating a cross-tabulation (contingency table) between group\_ discussion and final\_ exam\_ pass, we calculate two types of probabilities:



**Joint Probability:** The chance of two things happening at the same time.



P({No Discussion} cap {Fail})

P({No Discussion} cap {Pass})

P({Discussion} cap {Fail})

P({Discussion} cap {Pass})



**Marginal Probability:** The overall probability of a single event on its own.



Discussion Rates: P({Discussion}) and P({No Discussion})

Exam Rates: P({Pass}) and P({Fail})





**🔍 6. Relationship \& Dependency Assessments**



**Conditional Probability:** Shows how one event affects another. 



We check the passing rates under different conditions:



**Pass rate with discussion:** P({Pass} | {Discussion})

**Pass rate without discussion:** P({Pass} | {No Discussion})



**Dependency Logic:** We test if group discussions and passing the exam are independent using the multiplication rule:

Check if:  P({Discussion} cap {Pass}) = P({Discussion}) x P({Pass})



If the values are equal, the events are independent (they do not affect each other).

If they are different, the events are dependent (they influence each other).





**🧠 7. Bayes' Theorem Application**



If we know a student passed the final exam, we can use Bayes' Theorem to find the probability that they participated in group discussions.



Formula: 

&#x20;                  **P(Discussion ∣ Pass)= P(Pass∣Discussion)×P(Discussion)\\P(Pass)**

​

This helps us reverse-engineer the data to see how closely associated a passing result is with active group discussion.













































