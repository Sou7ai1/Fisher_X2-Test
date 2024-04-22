Homework 1: Statistical Analysis with A/B Testing


This Jupyter notebook provides a comprehensive guide to A/B testing, Fisher’s exact test, and the chi-squared test within the context of statistical analysis. It is designed to help you understand the process of A/B testing, from formulating a hypothesis to analyzing data and making informed decisions.


Overview


A/B Testing: Learn the steps involved in A/B testing, including setting up the experiment, collecting data, and interpreting the results.
Fisher’s Exact Test: Explore the mathematical derivation of formulas used in Fisher’s exact test and how to apply them to contingency tables.
Chi-Squared Test: Understand how to implement the chi-squared test using Python code to determine the significance of observed differences in data.


Key Themes


Comparison of website design versions to determine which one performs better in terms of user engagement.
Calculation of probabilities in contingency tables to analyze the results of A/B tests.
Application of statistical tests to assess the significance of the differences observed in the data collected from different versions of a website.
Getting Started
To get started, open the homework1.ipynb notebook in Jupyter and follow the instructions provided. The notebook contains detailed explanations and Python code to guide you through the statistical analysis process.

Prerequisites

Basic understanding of probability and statistics.
Familiarity with Python programming and Jupyter notebooks.
Contributing
Feel free to fork this repository, make changes, and submit pull requests. If you find any issues or have suggestions for improvement, please open an issue.


This Jupyter notebook contains solutions to three tasks related to probability and contingency tables. Let’s briefly describe each task:

Task 1: Deriving the Formula for Computing the Probability of Table 1
Given the contingency table Table 1:

Table

                Click YES	Click NO	Row sum
    Sample A       (a)	      (b)	     (a+b)
    Sample B	   (c)	      (d)	     (c+d)
    Sum	          (a+c)	     (b+d)	      (N)

We want to compute the probability that the table with results will have the same values as in Table 1 for given values of (a), (b), (c), and (d).

Approach:

We assume the null hypothesis that samples (A) and (B) were taken from the same probability distribution.
We’ll use the hypergeometric probability distribution to compute this probability.

Derivation:

The total number of visitors is (N = a + b + c + d).
The probability of observing the same values as in Table 1 is given by:
[ P(\text{observing same values as in Table 1}) = \frac{{\binom{{a+c}}{{a}} \cdot \binom{{b+d}}{{b}}}}{{\binom{N}{a+b}}} ]

This formula gives us the probability of observing the same values as in Table 1 under the null hypothesis.
Task 2: Implement the Function table_probability(t)
This function computes the probability of “Table 1” for a given 2-by-2 contingency table (t). The implementation follows the derived formula from Task 1 and handles both one-tailed and two-tailed tests.

Task 3: Compute Fisher’s and χ²-Test for “Table 2”
We have observed counts for “Table 2.” We need to compute the p-values for Fisher’s exact test and χ²-test. We’ll compare the results obtained with our implementation and the functions scipy.stats.fisher_exact() and scipy.stats.chi2_contingency().
License
This project is licensed under the MIT License - see the LICENSE file for details.