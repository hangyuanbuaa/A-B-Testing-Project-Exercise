# README
This is my Udacity Data Analyst Nanodegree Project **Analyze A/B Test Results**.

> A/B testing is a way to compare two versions of a single variable, typically by testing a subject's response to variant A against variant B, and determining which of the two variants is more effective.

## Review from Udacity 

Good links about A/B testing:
https://adespresso.com/guides/facebook-ads-optimization/ab-testing/
https://www.designforfounders.com/ab-testing-examples/
https://www.optimizely.com/optimization-glossary/ab-testing/

Some stats on A/B testing:
https://www.abtasty.com/blog/learn-from-5-ab-test-case-studies/

### Code Quality

PART I

To remove duplicate a good way is to use, https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.drop_duplicates.html

PART II

When possible, it is always more computationally efficient to use numpy built-in operations over explicit for loops. The short reason is that numpy -based operations attack a computational problem based on vectors by computing large chunks simultaneously.

Additionally, using loops to simulate 10000 can take a considerable amount of time vs using numpy https://softwareengineering.stackexchange.com/questions/254475/how-do-i-move-away-from-the-for-loop-school-of-thought

Fast code:
```
new_converted_simulation = np.random.binomial(n_new, p_new,  10000)/n_new
old_converted_simulation = np.random.binomial(n_old, p_old,  10000)/n_old
p_diffs = new_converted_simulation - old_converted_simulation
```

### Statistical Analyses

Considering the results of the statistical test (p-value) and the suggested p-critical. Since p-value > p-critical, we can't reject the null. http://www.itl.nist.gov/div898/handbook/prc/section1/prc131.htm

One-Tailed and Two-Tailed Results
https://stats.idre.ucla.edu/other/mult-pkg/faq/pvalue-htm/
