# T-Test

A T-Test is a statistical hypothesis test used to determine if there is a significant difference between the means of two groups. It is commonly used in experiments and research to compare the means of two samples.

## Types of T-Tests

1. **Independent T-Test**: Compares the means of two independent groups.
2. **Paired T-Test**: Compares the means of the same group at different times.
3. **One-Sample T-Test**: Compares the mean of a single group against a known mean.

## Assumptions

- The data is continuous.
- The data follows a normal distribution.
- The variances of the two groups are equal (for independent T-Test).
- The samples are independent (for independent T-Test).

## Formula

$$
t_k = \frac{\bar{x} - \bar{y}}{ s / \sqrt{n} }
$$

Where:
- $\bar{x}$ and $\bar{y}$ are the sample means.
- $s$ is the sample's standard deviation.
- $n$ is the sample's size
- $t_k$ is the t-statistic.

or more generally... 

$$
\frac{difference\:of\:means}{standard\:deviations}
$$

## Interpretation

- **p-value < 0.05**: Reject the null hypothesis, indicating a significant difference between the groups.
- **p-value ≥ 0.05**: Fail to reject the null hypothesis, indicating no significant difference between the groups.

## Example

```python
import scipy.stats as stats

# Sample data
group1 = [20, 21, 22, 23, 24]
group2 = [30, 31, 32, 33, 34]

# Perform independent T-Test
t_stat, p_value = stats.ttest_ind(group1, group2)

print(f"T-Statistic: {t_stat}, P-Value: {p_value}")
```

## Ways of getting a bigger t-score
* Bigger difference in means ($\bar{x} - \bar{y}$)
* Smaller standard deviations ($s$)
* Larger sample size ($\sqrt{n}$)

## One sample t-test
Test whether a set of numbers could have been drawn from a distribution with a specified mean.  Not appropriate for categoical data.

### Formula

$$
t_{n-1} = \frac{\bar{x} - \mu}{ s / \sqrt{n} }
$$

Where 
- $\bar{x}$ is the sample mean
- $\mu$ is the population mean
- $s$ is the sample standard deviation
- $n$ is the sample size
- $t_{n-1}$ is the t-statistic
- $n-1$ is the degrees of freedom
