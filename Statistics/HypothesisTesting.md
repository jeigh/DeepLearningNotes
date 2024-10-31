# Hypothesis Testing
## Basis of all inferential statistics

$$
\frac{signal}{noise}
$$

## Hypotheses
### Good Hypothesis Criteria
* Clear
* Specific
* Falsifiable
* Based on prior data or theory
* Leads to a statistical test
* A statement, not a question
* A prediction about the direction of an event
* Relevant for unobserved data or phenomena
* Relevant for understanding nature

### Null Hypothesis
* The default assumption
* The hypothesis that there is no effect or no difference
* $H_0$

### Alternative Hypothesis
* The hypothesis that there is an effect or a difference
* $H_A$

## Model
An equation that tries to explains some features in a dataset.

## IVs (Independent Variables)
Variable you are using to explain the DV

## DVs (Dependent Variables)
Variable you are trying to explain

## P-z Pairs

| Percent |  # of standard deviations
|---------|--------------------------
| 68.3%   |  2
| 95.4%   |  4
| 99.7%   |  6


| P Value            | Z Value | # of standard deviations
|--------------------|---------|-------------------------
| One-Tailed 0.05    | 1.64    | 1.96?
| Two-Tailed 0.05    | $\pm$ 1.96    | $\pm$ 2.58?
| One-Tailed 0.01    | 2.32    | 2.58?
| Two-Tailed 0.01    | $\pm$ 2.58    | $\pm$ 3.29?
| One-Tailed 0.001   | 3.09    | 3.29?
| Two-Tailed 0.001   | $\pm$ 3.29    | $\pm$ 3.89?

## Degrees of Freedom
The number of independent values or quantities which can be assigned to a statistical distribution.

* Determines the shape of the t-distribution.
* Higher df generally indicates more power to reject the null hypothesis.

Generally:  \
$df=n-k$

Where:
* $n$ is the number of observations (independent variables)
* $k$ is the number of parameters estimated for the model (dependent variables)
* $df$ is the degrees of freedom

### Significance Threshold ($\alpha$)
The imaginary vertical line that identifies whether or not the sample is statistically significant.


## Stastical Decisions
Given $\alpha$ (significance level) and $\beta$ (power), we can make the following decisions:

* **True Negative** The sample is within the significance threshold, and we assert that the null hypothesis is true. $(1-\alpha)$.  The sample is not statistically significant.

* **True Positive** The sample is beyond the significance threshold, and we assert that the null hypothesis is false. $(1-\beta)$.  The sample is statistically signficant.

* **Type 1 Errors** - False Positives; The sample is beyond the signifcance threshold, and we assert that the null hypothesis is false. The sample is statistically significant.

* **Type 2 Errors** - False Negatives;  The sample is within the significance threshold, and we assert that the null hypothesis is true. The sample is not statistically significant.

By increasing the significance threshold, both the true positives and false positives are decreased. \
By decreasing the significance threshold, both the true negatives and false negatives are increased.

## Parametric vs Non-Parametric Tests
Favor parametric tests over non-parametric tests when possible.

### Non-Parametric means...
* Statistics that are not based on assumptions about the distribution (eg... distribution is not gaussian)
* Statistical inference methods that generate the $H_0$ distrubiton from the data, not from an equation.

### Qualities of parametric tests:
* Standard, widely used
* Based on assumptions
* assumptions should be tested
* Can be incorrect when assumptions are violated
* Computationally fast
* Analytically Proven

### Qualities of non-parametric tests:
* Some are nonstandard
* Fewer assumptions are necessary
* Can be slow/intensive
* Appropriate for non-numeric data
* Appropriate for small sample sizes
* Some methods give nondeterministic results

## Multiple Comparisons
**Familywise Error Rate (FWEor FWER)** - The probability of making one or more false discoveries, or Type I errors, among all the hypotheses when performing multiple hypotheses tests.

$$
FWE \leq 1 - (1 - \alpha)^n \leq n \alpha
$$

where
* $FWE$ is the familywise error rate,
* $\alpha$ is the significance level,
* $n$ is the number of tests.


### Bonferroni Correction
A method used to counteract the problem of multiple comparisons.  It is a simple and conservative method that adjusts the significance level by dividing it by the number of comparisons.

$$
\alpha_{new} = \frac{\alpha}{n}
$$

where   
* $\alpha_{new}$ is the new significance level,
* $\alpha$ is the original significance level,
* $n$ is the number of comparisons.



## Cross Validation
Breaking up the data into training and testing sets to validate the model.
* **Training Set** - The data used to train the model.
* **Testing Set** - The data used to test the model.


## Statistical Significance vs Classification Accuracy 


