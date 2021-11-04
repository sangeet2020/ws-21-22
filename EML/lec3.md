# Lecture 3

## Linear regression

- which predictors are helpful
    - use hypothesis test to test for a subset of predictors.
    - use F statistic
    - T statistic
        - measure the added effect of the variable in question, when all other variable are in the model.
    - in high dim we cannot restrict ourselves to the $p$ values of individual variables.

- Selecting important variables
    - variable selection or feature selection
    - create all possible subsets
        - {}, {TV}, {radio}, {newspaper}, {TV, radio}, {radio, newspaper}...
        - $2^p$ subsets
        - way too many models
    - feature selection
        - forward selection
            - being with empty feature set
            - fit $p$ models, one for each variable
            - select model with lowest RSS
            - try adding each of the remaining $p-1$ variables inot this model
            - pick the one with lowest RSS
            - continue until a criterion is filled
        - backward selection
        - model selection

- how well the model fits the data
    - RSE and $R^2$
    - for univariate
    - for multivariate
    - if $R^2$ is 1..we are perfectly happy
    - problems
        - increases if we add variables
        - we need to focus ion test error
    - Coefficient intervals
        - compute CI for coefficients and for the output
    - when the relationship between input and output is non-linear, any linear model will incur a bias and the reducible error can be reduced with a non-linear model
    - even when the true relationship between input and output is known the we can not remove irreducuble error
    - PS: no need to remember formulas for CI and PI

- non-linear relationship
    - the function of the inputs used by a model are called base function

## Regression pitfalls
- P1: Non-linearity
    - if data is non-linear, linear models are never exact fit
    - residual plots can help identify nonlinearity
    - important from exam point of view
    - plot residual error against the fitted output values

- P2: correlation of error terms
    - the theory of linear models ersts on the assumption that the erros are uncorrelated
    - if this is not the case, standard errors tend to be larger than given by the formulas

- P3: Non constant variance of errors
    - rewuired that $var =\sigma^2$ is constant is central for the theory on linear models
    - changing variance is called heteroscedacticity
    - the varaince of the error increases with the size of the response.
- P4: outliers
    - outcome is far from prediction

- P5: high leverage points
    - points with unusual input values.
    - removing high leverage points has large impact on the regression line
    - important to identify these points
    - compute leverage statistic

- P6: Collinearity
    - if two or more predictors are closely related they are collinear.
    - collinear variables can substitute each other i.e. trade parts of their coefficients.
