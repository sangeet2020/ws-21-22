# Lecture 7: Regularization

- we can expand on the basic linear model in several ways
- make model more flexible
  - add i non-linear basic functions
  - keave the linear paradigm
- make model less flexible
  - subset selection
  - shrinkage: penalize model with large coefficients to prefer and select model with smaller coefficients
  - dimension reduction

### Why simpler models

- Gauss markov theorem: linear model is unbiased with smallest variance
- bias variance tradeoff.
  - reduce variance at the cost of slight inc in bia

### Best subset selection
- find best model for every possible subset of predictors
- we can also do this by regularization
- Forward step wise selection
    - Greedy approach

### Choosing optimal model
- least square model: Cp statistic
- penatly inc with the number of predictors and the variance of the irreducible error.
- this accounts for the possibility of overtraining
- Akaike's information criterion (AIC)
    - for least square model with Gaussian errors, the maximum  likelihood and least square approaches are equivalent.
- Bayesian information center

### Ridge Regression
- 