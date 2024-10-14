## Common Distribution Types

### Power Law Distribution
A continuous probability distribution that describes the probability distribution of a random variable.  Also called the Pareto distribution.

$$  P(x) = C x^{-\alpha} $$
where:

* $ P(x) $ is the probability of the random variable $ x $,
* $ C $ is a normalization constant,
* $ \alpha $ is a positive parameter that characterizes the distribution.

### Normal Distribution 
A continuous probability distribution that is symmetric about the mean.  Also called the Gaussian distribution.

$$ 
P(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} 
$$

where:

* $ P(x) $ is the probability density function,
* $ \mu $ is the mean of the distribution,
* $ \sigma $ is the standard deviation of the distribution,
* $ e $ is the base of the natural logarithm (approximately equal to 2.71828).

### Uniform Distribution: 
A continuous probability distribution that is defined by two parameters: the minimum and maximum values. Also called the rectangular distribution.

$$ 
P(x) = \frac{1}{b-a}
$$

where:

* $ P(x) $ is the probability density function,
* $ a $ is the minimum value,
* $ b $ is the maximum value.

### Chi-Squared Distribution
A continuous probability distribution that describes the sum of squared standard normal deviates.

$$
P(x) = \frac{1}{2^{k/2} \Gamma(k/2)} x^{(k/2)-1} e^{-x/2}
$$

where:

* $ P(x) $ is the probability density function,
* $ k $ is the degrees of freedom,
* $ \Gamma $ is the Gamma function,
* $ e $ is the base of the natural logarithm (approximately equal to 2.71828).


### Student's t-Distribution
A continuous probability distribution that describes the mean of a normally distributed population when the sample size is small.  

$$ 
P(t) = \frac{\Gamma\left(\frac{\nu + 1}{2}\right)}{\sqrt{\nu \pi} \Gamma\left(\frac{\nu}{2}\right)} \left(1 + \frac{t^2}{\nu}\right)^{-\frac{\nu + 1}{2}} 
$$

where:

* $ P(t) $ is the probability density function,
* $ \nu $ is the degrees of freedom,
* $ \Gamma $ is the Gamma function,
* $ t $ is the variable.

In the context of the Student's t-distribution, the Gamma function $ \Gamma $ is a special mathematical function that generalizes the factorial function to real and complex numbers. It is defined as:

$$ \Gamma(n) = \int_0^\infty t^{n-1} e^{-t} , dt $$

For positive integers, the Gamma function satisfies $\Gamma(n) = (n-1)!$. In the Student's t-distribution equation the Gamma function is used to normalize the distribution and ensure that the total area under the probability density function is equal to 1.

### F-Distribution
A continuous probability distribution that describes the ratio of two independent chi-squared distributions.

$$
P(F) = \frac{\left(\frac{d_1}{d_2}\right)^{d_1/2} \left(F\right)^{(d_1/2)-1}}{B\left(\frac{d_1}{2}, \frac{d_2}{2}\right) \left(1 + \frac{d_1}{d_2}F\right)^{(d_1+d_2)/2}} 
$$ 

where:

* $ P(F) $ is the probability density function,
* $ d_1 $ and $ d_2 $ are the degrees of freedom for the numerator and the denominator, respectively,
* $ B $ is the Beta function,
* $ F $ is the variable.

In the context of the F-distribution, the Beta function $ B $ is a special mathematical function that generalizes the concept of binomial coefficients to real and complex numbers. It is defined as:

$$ B(x, y) = \int_0^1 t^{x-1} (1-t)^{y-1} , dt $$

Alternatively, it can be expressed in terms of the Gamma function:

$$ B(x, y) = \frac{\Gamma(x) \Gamma(y)}{\Gamma(x + y)} $$

In the F-distribution equation, the Beta function is used to ensure that the total area under the probability density function is equal to 1, thereby normalizing the distribution.

### Log-Normal Distribution 
A continuous probability distribution that is the logarithm of a normal distribution.  Also called the Galton distribution.
$$
P(x) = \frac{1}{x \sigma \sqrt{2\pi}} e^{-\frac{(\ln(x)-\mu)^2}{2\sigma^2}}
$$
where:

* $ P(x) $ is the probability density function,
* $ \mu $ is the mean of the natural logarithm of the variable,
* $ \sigma $ is the standard deviation of the natural logarithm of the variable,
* $ \ln(x) $ is the natural logarithm of ( x ),
* $ e $ is the base of the natural logarithm (approximately equal to 2.71828).



## Uncommon Distribution Types (AI-Generated)
* **Triangular Distribution**: A continuous probability distribution that describes the probability distribution of a random variable.  

* **Hyperbolastic Distribution**: A continuous probability distribution that describes the probability distribution of a random variable. 

* **Binomial Distribution**: A discrete probability distribution that describes the number of successes in a fixed number of Bernoulli trials.  Also called the Bernoulli distribution.

* **Poisson Distribution**: A discrete probability distribution that describes the number of events in a fixed interval of time or space.

* **Exponential Distribution**: A continuous probability distribution that describes the time between events in a Poisson process.  



* **Beta Distribution**: A continuous probability distribution that describes the probability distribution of a random variable limited to a finite interval.  Also called the Euler distribution.

* **Gamma Distribution**: A continuous probability distribution that describes the time until a specified event occurs.  Also called the Erlang distribution.

* **Weibull Distribution**: A continuous probability distribution that describes the time until a specified event occurs.  Also called the Rosin-Rammler distribution.

* **Logistic Distribution**: A continuous probability distribution that describes the probability distribution of a random variable.  Also called the logit-normal distribution.

* **Cauchy Distribution**: A continuous probability distribution that describes the ratio of two independent standard normal deviates.  Also called the Lorentz distribution.

* **Laplace Distribution**: A continuous probability distribution that describes the probability distribution of a random variable.  Also called the double exponential distribution.

* **Gumbel Distribution**: A continuous probability distribution that describes the probability distribution of a random variable.  Also called the extreme value distribution.

* **Log-Logistic Distribution**: A continuous probability distribution that describes the probability distribution of a random variable.  Also called the Fisk distribution.

* **Rayleigh Distribution**: A continuous probability distribution that describes the probability distribution of a random variable. Also called the Rayleigh-Gans distribution.

* **Exponential Power Distribution**: A continuous probability distribution that describes the probability distribution of a random variable.  Also called the Subbotin distribution.
