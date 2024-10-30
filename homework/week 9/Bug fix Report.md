#### Group Members: Sizar, Abrar, Sinha
#### GH Repo: PyCaret

### **Explanation of the Bug, Fix, and Solution in PyCaret Issue \#3011**

**Issue Summary:** The original issue, PyCaret Issue \#3011, revolved around an incorrect display of the fold count in the setup summary when using certain cross-validation (CV) strategies, specifically `ExpandingWindowSplitter`, in the `pycaret.time_series` module. Instead of displaying a numeric fold count, the setup summary showed the entire `ExpandingWindowSplitter` object in the "Fold Number" field. This created confusion, as users expected to see the actual number of folds rather than a complex object reference.

### **1\. Reproducing the Issue**

To reproduce the issue, the following code snippet can be used:

```bash
# !pip install pycaret==3.0.0rc3

import numpy as np
from pycaret.time_series import TSForecastingExperiment
from pycaret.datasets import get_data
from sktime.forecasting.model_selection import ExpandingWindowSplitter

y = get_data(114, folder="time_series/seasonal", verbose=False)
cv = ExpandingWindowSplitter(fh=np.arange(1, 13), initial_window=24, step_length=4)
exp = TSForecastingExperiment()
exp.setup(y, fh=12, fold=cv)
```

* **Dataset Used:** get_data(114, folder="time_series/seasonal") loads a time series dataset with 171 data points. This dataset is univariate, meaning it consists of a single variable, which we aim to forecast over future time steps.
* **Expanding Window Cross-Validation Setup:**  
  * ExpandingWindowSplitter is a type of cross-validation strategy where each fold gradually expands the training window by a specified step length.
  * initial_window=24: The first training window contains 24 data points.
  * step_length=4: Each fold expands the training window by 4 additional data points. 
  * fh=np.arange(1, 13): The forecasting horizon predicts the next 12 data points after each training window.

The issue manifests when the experiment is set up using this code. Instead of showing the number of folds used in cross-validation, the setup summary incorrectly displays the ExpandingWindowSplitter object.

Expected Example Output:
For a dataset of length [171,0], the fold number output should be 31. Instead it displays, "ExpandingWindowSplitter(fh=array([ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]), initial_window=None, step_length=4)"

### **2. Root Cause of the Issue**

The root cause of the issue lies in how PyCaret's _setup_fold_generator function was handling the fold parameter:

Here is the original function from the source code:

```bash
    def _set_fold_generator(self) -> "TSForecastingExperiment":
        """Sets up the cross validation fold generator that operates on the training dataset.

        Returns
        -------
        TSForecastingExperiment
            The experiment object to allow chaining of methods

        Raises
        ------
        TypeError
            When the fold_strategy passed by the user is not one of the allowed types
        """
        possible_time_series_fold_strategies = ["expanding", "sliding", "rolling"]
        #TODO: Change is_sklearn_cv_generator to check for sktime instead
        if not (
            self.fold_strategy in possible_time_series_fold_strategies
            or is_sklearn_cv_generator(self.fold_strategy)
        ):
            raise TypeError(
                "fold_strategy parameter must be either a sktime compatible CV generator "
                f"object or one of '{', '.join(possible_time_series_fold_strategies)}'."
            )

        if self.fold_strategy in possible_time_series_fold_strategies:
            # Number of folds
            self.fold_param = self.fold
            self.fold_generator = self.get_fold_generator(fold=self.fold_param)
        else:
            self.fold_generator = self.fold_strategy
            # Number of folds
            self.fold_param = self.fold_strategy.get_n_splits(y=self.y_train)

        return self
```

* The code is directly setting the Fold Number in the summary by assigning the self.fold attribute to fold_param. 
* This approach works fine for simpler fold strategies, such as when using an integer-based fold count. However, it did not account for complex splitter objects, such as ExpandingWindowSplitter, where self.fold is an object that manages the splitting process rather than a simple number.

In this case, because ExpandingWindowSplitter is an object that dynamically generates folds based on the dataset's characteristics (length, initial window, step length, and forecasting horizon), the setup summary displayed the entire object reference instead of calculating and showing the actual number of folds.

### **3. Steps Taken to Fix the Issue**

To fix the issue, the _set_fold_generator method was modified. The updated method calculates the actual fold count when using complex cross-validation objects like ExpandingWindowSplitter.

### **4. Solution Implementation**

Here is the revised _set_fold_generator function with the necessary changes:

```bash
def _set_fold_generator(self) -> "TSForecastingExperiment":`

    `"""Sets up the cross-validation fold generator that operates on the training dataset."""`

    `possible_time_series_fold_strategies = ["expanding", "sliding", "rolling"]`

    `if not (`

        `self.fold_strategy in possible_time_series_fold_strategies`

        `or is_sklearn_cv_generator(self.fold_strategy)`

    `):`

        `raise TypeError(`

            `"fold_strategy parameter must be either a sktime compatible CV generator "`

            `f"object or one of '{', '.join(possible_time_series_fold_strategies)}'."`

        `)`

    `if self.fold_strategy in possible_time_series_fold_strategies:`

        `# Adjust fold_param based on calculated splits`

        `self.fold_generator = self.get_fold_generator(fold=self.fold)`

        `self.fold_param = (`

            `self.fold_generator.get_n_splits(y=self.y_train)`

            `if hasattr(self.fold_generator, 'get_n_splits') else None`

        `)`

    `else:`

        `self.fold_generator = self.fold_strategy`

        `self.fold_param = self.fold_generator.get_n_splits(y=self.y_train)`

    `return self`
```

### **5. Explanation of the Solution**

* **Calculating Fold Count Dynamically:** The function now calculates the number of folds dynamically using get_n_splits(y=self.y_train), which returns an integer representing the actual number of folds used in cross-validation.
* **Compatibility Check:** Before calculating the fold count, a compatibility check is performed using hasattr to ensure that the fold_generator supports the get_n_splits method. If not, the fold_param is set to None. 
* **Correct Display in Setup Summary:`** `This solution ensures that the "Fold Number" in the summary accurately displays the number of folds, even when using advanced cross-validation strategies like ExpandingWindowSplitter.

### **6. Step-by-Step Calculation of Fold Count**

For a dataset with 171 data points:

* **Initial Window:** The first training window contains 24 points (initial_window=24).
* **Step Length:** Each subsequent fold expands the training window by 4 additional points (step_length=4). 
* **Forecast Horizon:** The prediction window spans the next 12 data points (fh=12).
* **Fold Count Calculation:** Starting with 24 points and adding 4 points for each new fold, the total number of folds that can fit into the dataset until only 12 data points are left for forecasting is 31.

### **7. Why This Solution Fixes the Issue**

By explicitly calculating fold_param using the get_n_splits method, the solution avoids displaying the object reference in the setup summary. It dynamically adapts to the dataset length and cross-validation parameters, ensuring that more complex cases are handled correctly.

### **8. Solution Discovery Process**

* **Identifying the Issue Source:** The initial setup incorrectly displayed the "Fold Number" as the cross-validation object. 
* **Debugging Steps:** Print statements were added to trace the values of fold_param and fold_generator, helping identify where the incorrect assignment occurred. 
* **Consulting Documentation:** The documentation for ExpandingWindowSplitter was reviewed, revealing that get_n_splits(y=...) can provide the actual number of splits.
* **Testing:** The solution was implemented and verified to show the correct fold count for various cross-validation strategies, including the modified code.

### **9. Conclusion**

The bug in PyCaret's pycaret.time_series module was caused by directly displaying complex cross-validation objects instead of calculating the fold count. The fix involved updating the _set_fold_generator function to determine the number of folds dynamically, ensuring that the "Fold Number" in the setup summary reflects the actual number of folds, even when using sophisticated CV strategies like ExpandingWindowSplitter. This solution enhances the usability and interpretability of PyCaret's time series experiment setup, providing users with more accurate information.


