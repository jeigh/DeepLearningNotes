# Probability
Probability is a numerical description of how likely an event is to occur or how likely it is that a proposition is true.  Probability is a number between 0 and 1 where 0 indicates impossibility and 1 indicates certainty.

Descrete, Ordinal, and Nominal data types are appropriate for probability calculations.
Interval and Ratio data types are not appropriate for probability calculations.

$$
p_i = \frac{100 \times c_i}{\Sigma c}
$$

where
* $ p_i $ is the probability of event $ i $,
* $ c_i $ is the count of event $ i $,
* $ \Sigma c $ is the total count of all events.

## Odds
Odds are a measure of the likelihood of an event occurring. They are the ratio of the probability of an event occurring to the probability of it not occurring.
$$
r = n : m = \frac{n}{m}
$$

where:
* $r$ is the odds,
* $m$ is the probability of the event occurring,
* $n$ is the probability of the event not occurring.

or...

$$
r=\frac{1-p}{p}
$$

where:
* $r$ is the odds,
* $p$ is the probability of the event occurring.

therefore:

$$
p=\frac{m}{m+n}
$$

## Probability Mass Function
for discrete data; more relevant for science and engineering

## Probability Density Function
for continuous data;  smooth curve;  more relevant for theoretical math

## Cumulative Distribution Function
The cumulative distribution function (CDF) is a function that gives the probability that a random variable takes on a value less than or equal to a given value. It is used to describe the distribution of a random variable.

Essentially it's the integral of the PDF from zero to the value of interest.

$$
C(x_a) = \int_{-\infty}^a{p(x_t)dt} \\
$$ 
or 
$$
C(x_a) = \sum_{i=1}^a p(x_i)
$$

## Sample distribution
the mean of means of samples

## Monte-Carlo Sampling
Monte Carlo methods are a broad class of computational algorithms that rely on repeated random sampling to obtain numerical results. Their essential idea is using randomness to solve problems that might be deterministic in principle. They are often used in physical and mathematical problems and are most useful when it is difficult or impossible to use other approaches.

Emphasis on the fact that getting the actual population is not possible, so we use a sample to estimate the population.

## Expected Value
It is a measure of the center of the distribution of the variable. It is the weighted average of all possible values of the variable, where the weights are the probabilities of the values occurring.

$$
E[X] = \sum_{i=1}^n x_i p_i
$$
where
* $E[X]$ is the expected value of the variable $X$,
* $x_i$ is the value of the variable $X$,
* $p_i$ is the probability of the value $x_i$ occurring.

### Average vs Expected Value
* Average is an empirical sample estimate
* Expected value is a theoretical population estimate


## Conditional Probability
$$
P(A|B) = \frac{P(A \cap B)}{P(B)} \\
P(A \cap B) = P(A|B) \times P(B) 
$$

where
* $P(A|B)$ is the probability of event $A$ given event $B$,
* $P(A \cap B)$ is the probability of event $A$ and event $B$,
* $P(B)$ is the probability of event $B$.


## The law of large numbers
As the number of trials increases, the experimental probability of an event approaches the theoretical probability of the event.

$$
\lim_{n \to \infty} P(|P\bar{x}_n - \mu | > \epsilon) = 0
$$

where
* $P\bar{x}_n$ is the sample mean,
* $\mu$ is the population mean,
* $\epsilon$ is the error.

## The central limit theorem
All sample means are normally distributed.  The larger the sample size, the closer the sample mean is to gaussian.




