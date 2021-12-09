# Lecture 6

### Validation set approach
- randomly divide data into train and test
- model is fit on train
- test error on test
- elbow rule
- observation
    - test error can vary widely
    - quadratic term affords large improvement of test error
    - higher order terms not of benefit
- problems
    - high variability of estimated test error
    - smaller train set -> model may be under trained i.e. suboptimal.

### Leave one out cross validation
- we train the model on same dataset except one data point
- advantages
    - train set is as large as can be, thus there is a little bias
- problem
    - because only one point is tested, there is a high variance.
- determininistic process.
    - repeating yields the same result
- variance of the test errors get reduced by averaging over each fold.


### k fold Cross validation
- randomly divide data ubti k folds
- this gives k estimates of the test error