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
Will post the proposed solution in the thread of the issue. Hoping to have some discussions with contributors regardind my theoretical understanding of the isuue as well as the model's source code.

## Detailed Explanation of the Fix:

### Overview/Recap
The author of the issue talked about an unexpected behavior that they encountered while using the Bayesian Ridge Model from the linear models of scikit learn machine learning library. The predictive standard deviation (ystd) was dependent on the scale of uniform sample_weight. This behavior contradicted expectations, as uniform sample weights should not alter the model's predictive uncertainty, only the relative importance of data points. 

### Understanding the Original Source Code
The source code of the Bayesian Ridge model is located inside the linear models subdirectory of the scikit learn library. Much of my understanding of the functionality of the code came from my theoretical background from Bayesian Statistics class. While I do not possess a full understanding of each and every line of the source code, it was enough to locate the lines that used sample weights and then I made changes in them. 

The Bayesian Ridge model is defined as a class and below are the functions which I focused on (there were some other functions too but I didnt look at them for this issue):
1. Training (fit method):
   - It trains the input data points and fits the model.
   - Uses prior assumptions and prior likelihood of the input data to computes posterior distributions of the input data.
   - It also iteratively updates hyperparameters (alpha, lambda) to improve the model’s estimates. (this part was important to understand since adjustment to alpha was the noise parament and it was important).
2. Prediction (predict method):
   - Computes the mean (ymean) and standard deviation (ystd) of the predictive posterior distribution using the posterior covariance matrix (sigma_) and the noise precision (alpha_).

### Sample Weights:
It is initialized in the fit method and it modifies the influence of each data point during training. Using the provided sample weights, the input data is rescaled appropriately.
  
The original source code inadvertently allowed the absolute scale of uniform sample_weight to affect the predictive standard deviation, introducing the unintended behavior.

### Initial Understanding of the Issue:
When examining the issue, I observed the following:
1. Uniform weights (sample_weight=np.ones(size)) produced a reasonable predictive standard deviation.
2. Scaling these weights (e.g., sample_weight=20 * np.ones(size)) caused the predictive standard deviation to increase too, suggesting reduced confidence in predictions.


### How did I understand that I need to work on the preprocessing of sample weights and noise precision?
I examined how the standard deviation of the predicted y (y_std) was calculated and traced the code backward to understand its connection to sample weights. I found that the application of sample weights during the preprocessing stage, along with the calculation of input data noise, directly influences the final **y_std**.

### Solution Implementation
To resolve this, I tried to **normalize the sample weights** and **adjust the effective sample size**. **The key was ensuring that uniform weights act only as relative importance indicators, without altering the scale of alpha_ or sigma_ (which are the essential hyperparamenters)**.
1. Normalization of Sample Weights: I normalized the weights by dividing them by their mean.
   
Before:
```
if sample_weight is not None:
            sample_weight = _check_sample_weight(sample_weight, X, dtype=dtype)
```
After:
```bash
if sample_weight is not None:
            sample_weight = _check_sample_weight(sample_weight, X, dtype=dtype)
            sample_weight = sample_weight / np.mean(sample_weight)
```
This ensured that the absolute scale of uniform weights did not affect the calculations, preserving only their relative importance.

2. Effective Sample Size:
I  added a new variable “effective_sample_size” to compute the total influence of weighted data:
```bash
 if sample_weight is not None:
            effective_sample_size = np.sum(sample_weight)
        else:
            effective_sample_size = X.shape[0]
```
This replaced the unweighted n_samples in calculations that also connects to the noise precision (alpha_), ensuring proper scaling.

3. Modification of alpha_:
I modified the formula for updating the noise precision to incorporate the effective sample size:

Before:
```bash
alpha_ = (n_samples - gamma_ + 2 * alpha_1) / (rmse_ + 2 * alpha_2)
```
After:
```bash
alpha_ = (effective_sample_size - gamma_ + 2 * alpha_1) / (rmse_ + 2 * alpha_2)
```
This ensured that uniform weights had no unintended impact on noise variance.

### Behavior After Fix:
   - The scale of uniform weights no longer affected ystd, making it independent of the absolute values of sample_weight.
   - The predictive mean (ymean) remained consistent, as the weights still preserved the relative importance of data points.




