## Solo Fix Progress Report 3

#### Codebase: [Scikit-Learn](https://github.com/scikit-learn/scikit-learn)
#### Issue: [#24313](https://github.com/scikit-learn/scikit-learn/issues/24313)
#### Issue Topic: Standard Deviation of Bayesian Ridge Regression Model’s Predictions Affected by Uniform Sample Weights
#### Expected Behavior: Applying uniform sample weights should not affect the prediction’s standard deviation.
#### Actual Behavior: The standard deviation increases proportionally to the uniform weight applied to samples.
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Progress:
Found the solution to the issue.

## Next Step:
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Detailed Explanation of the Fix:

### Overview/Recap
The author of the issue talked about an unexpected behavior that they encountered while using the Bayesian Ridge Model from the linear models of scikit learn machine learning library. The predictive standard deviation (ystd) was dependent on the scale of uniform sample_weight. This behavior contradicted expectations, as uniform sample weights should not alter the model's predictive uncertainty, only the relative importance of data points. 
