# Lecture 1

## Pre-lecture prep
## Basic ML settings
- regression
- classification
    - predict a class
    - predict whole distribution of all class probabilities
- optimization: goal is to match the training set as well as possible
- but goal of ML is perform on unseen/new data
    - achieve low generalization error
## Notation
- a- scalar
- ***a***- vector
- ***A*** - matrix
- **A** - tensor

===================
## Applications of Statistical learning
- how can we do predition
- eda: exploratory data analysis
- inference

## Introduction
Relationship between X and Y is given as:
$$
y = f(x) + \epsilon = f(X_1 , X_2, X_3..., X_p) + \epsilon 
$$
$\epsilon$ is the general additive term

- the best line defining the data depends on how we define "best" or what  are we trying to model

## Why estimate $f$?
- $X$ are inputs that is given and $Y$ are outputs are desired.
$$
E[X-\hat{Y}] = E[f(x)+\epsilon- \hat{f}(x)]
$$
- goal of prediction is to minimize the reducible error
- the reducible error can not be avoided.
- treat $\hat{f}(x)$ as blackbox
- the goal is to understand the relation of input and output

### Inference
- observe relationship between each predictor and response.
    - is it complicated or linear
- prediction and inference are of equal importance to us but comes with a tradeoff. A linear inference may be easy to interpret but may be not accurate.

- estimating $\hat{f}$ is coming up with a function that best explains the data or observation $(X,Y)$
- its about how many degree of freedom the data has: parametric and nonparametric
    - parametric methods
        - has  a functional form like a linear model
        $$
        f(x) = \beta_0 + \beta_1X_1 + \beta_2X_2 + ...\beta_pX_p
        $$
        -
    - non-parametric methods
        - we aim at finding the form of $f$
        - choosing the form gives us much more freedom

### Acc vs Interpretability
- check graph: flexibility vs interpre.
- highly felxible model needs more data
- a flexible models entails a large number of parameters.
-  with few observation we choose less flexible model.
- semi-supervised learning
    - same as supervised but also leverages unlabeled data.
    - uses cluster analysis.

### Model accurayc
- MSE
- test error/prediction error/ expected prediction error.

### Bias variance tradeoff
- see proof
- Low training error
    - high variance
- High training / test error
    - high bias
- our goal while training
    - low bias and low variance
    - if trained excessively i.e overfitting
        - high variance and low bias

### Classification setting
- measuring classification error is called as misclassification error.






















