# Data Analysis

## Ensemble Learning

### Bagging
- Bagging is where multiple models are trained on the same dataset and the final prediction is the average of the predictions of all the models.
- Stands for "Bootstrap Aggregating".

### Boosting
- Multiple models are trained sequentially and the final prediction is the weighted average of the predictions of all the models.  The subsequent models are trained on the errors of the previous models.

### Bucket of models
- A bucket of models is where multiple different models are trained on the same dataset and the final prediction is whichever model is the best.

### Stacking
- Stacking is where multiple models are trained on the same dataset and the final prediction is the average of the predictions of all the models.


## Advanced Ensemble Learning
### Bayes Optimal Classifier
- The Bayes Optimal Classifier is the best possible classifier for a given dataset.  It is the classifier that has the lowest possible error rate.
- It's usually impractical because of computational requirements.

### Bayesian Parameter Averaging
- Bayesian Parameter Averaging is where the parameters of multiple models are averaged to create a new model.

### Bayesian Model Combinations
* tries to address all of the above two problems

## XGBoost
* Extreme Gradient Boosted Trees
* Uses regularized boosting which prevents overfitting
* Can handle missing values automatically
* Parallel Processing
* can cross-validate at each iteration (early stopping, optimal number of iterations)
* Incremental Training
* plug in your own optimization objectives
* tree pruning (results in deper, optimized trees)


### Hyperparameters
* Booster (glibtree or gblinear)
* Objective (softmax, softprob)
* Eta $\Eta$  (learning rate)
* Max Depth (depth of the tree)
* min_child_weight (can control overfitting)
* others...

## Support Vector Machines
* Supervised Learning
* Good for many dimensions
* Kernel Trick - representing ata in higher dimensional spaces to find hyperplanes that are not apparent in lower dimensions.


# Correlation / Covariance Analysis
* a correlation analysis computes a correlation coefficient (termed "r")
* r ranges from -1 to 1
* r = 1 means a perfect positive correlation
* r = -1 means a perfect negative correlation
* r = 0 means no correlation
* Correlation is normlized (scale -1 to 1, where 0 means no correlation)
* Covariance is not normalized (scale from - $\infin$ to $\infin$).
* Covariance of datasets whose values are all z-scored is the same as correlation.

### Covariance Formula:
$$
c = \frac{1}{n-1}\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})
$$

### Correlation Coefficient Formula:
$$
r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2 \sum_{i=1}^{n} (y_i - \bar{y})^2}}
$$

where
* $x_i$ is the ith value of x
* $\bar{x}$ is the mean of x
* $y_i$ is the ith value of y
* $\bar{y}$ is the mean of y
* n is the number of values in x and y

### P-value of correlation coefficient formula:
$$
t_{n-2} = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}
$$

where
* $t_{n-2}$ is the t-value
* r is the correlation coefficient
* n is the number of values in x and y

### Relationship between covariance and correlation matrices:

$$
C = \Sigma R \Sigma
$$
and...
$$
\Sigma^{-1} C \Sigma^{-1} = R
$$

Where
* $C$ is the covariance matrix 
* $\Sigma$ is the standard deviation matrix  (diagonal matrix)
* $R$ is the correlation matrix 


## Partial Correlation
* Partial correlation is the correlation between two variables after removing the effect of one or more other variables.

### Formula:
$$
r_{xy|z} = \frac{r_{xy} - r_{xz}r_{yz}}{\sqrt{1-r_{xz}^2}\sqrt{1-r_{zy}^2}}
$$

where
* $r_{xy|z}$ is the partial correlation between x and y controlling for shared variance with z
* $r_{xy}$ is the correlation between x and y
* $r_{xz}$ is the correlation between x and z
* $r_{yz}$ is the correlation between y and z

## Spearman's Rank Correlation
* Spearman's Rank Correlation is a non-parametric measure of correlation that is based on the ranks of the data values.
* it is monotonic.

Monotonic - a function is monotonic if it is either entirely non-increasing or non-decreasing.

step 1: rank the data
step 2: calculate the difference between the ranks of each pair of values
step 3: calculate the Spearman's Rank Correlation

### Formula:
$$
r_s = 1 - \frac{6\sum_{i=1}^{n} d_i^2}{n(n^2-1)}
$$

where
* $r_s$ is the Spearman's Rank Correlation
* $d_i$ is the difference between the ranks of the ith pair of values
* n is the number of values

## Fisher Z-Transformation
* Fisher Z-Transformation is a method of transforming correlation coefficients so that they are normally distributed.

$$
Z = \frac{1}{2} \ln \left( \frac{1+r}{1-r} \right)
$$
    
where
* Z is the Fisher Z-Transformation
* r is the correlation coefficient

## Kendall's Correlation
* Kendall's Correlation is a non-parametric measure of correlation that is based on the ranks of the data values.
* only use it for ordinal data (not continuous or descrete data)

$$
\tau = \Kappa^{-1} \sum \text{sgn}(\tilde x_i - \tilde x_{i:}) \text{sgn}(\tilde y_i - \tilde y_{i:})
$$

Where
* $\tau$ is the Kendall's Correlation
* $\Kappa$ is the number of pairs of values
* $\tilde x_i$ is the rank of the ith value of x
* $\tilde x_{i:}$ is the average rank of the values of x that are tied with the ith value of x
* $\tilde y_i$ is the rank of the ith value of y
* $\tilde y_{i:}$ is the average rank of the values of y that are tied with the ith value of y

## Subgroups correlation paradox
* The subgroups correlation paradox is where the correlation between two variables is positive when the data is split into subgroups, but negative when the data is not split into subgroups.

## Cosine Similarity
* Cosine Similarity is a measure of similarity between two non-zero vectors of an inner product space that measures the cosine of the angle between them.

Formula:
$$
cos(\theta) = \frac{\sum_{i=1}^{n} x_i y_i}{\sqrt{\sum_{i=1}^{n} x_i^2} \sqrt{\sum_{i=1}^{n} y_i^2}}
$$



# ANOVA
* ANOVA (Analysis of Variance) is a statistical test used to determine if there are any statistically significant differences between the means of three or more independent groups.

<number>-way ANOVA
* A 1-way ANOVA is used when there is only one independent variable.
* A 2-way ANOVA is used when there are two independent variables.
* etc...

