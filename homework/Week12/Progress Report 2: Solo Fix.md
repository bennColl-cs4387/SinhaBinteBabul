## Solo Fix Progress Report 2

#### Codebase: [Scikit-Learn](https://github.com/scikit-learn/scikit-learn)
#### Issue: [#24313](https://github.com/scikit-learn/scikit-learn/issues/24313)
#### Issue Topic: Standard Deviation of Bayesian Ridge Regression Model’s Predictions Affected by Uniform Sample Weights
#### Expected Behavior: Applying uniform sample weights should not affect the prediction’s standard deviation.
#### Actual Behavior: The standard deviation increases proportionally to the uniform weight applied to samples.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

Progress/Challenge:
In my previous progress report, I mentioned difficulties in replicating the issue, which stemmed from challenges in building scikit-learn from source. To address this, I had to rebuild scikit-learn five times using different approaches, such as adjusting build steps, testing various virtual environments, and troubleshooting dependency issues. The main problem was with the meson package, which is essential for compiling the Cython and C++ libraries. Initially, meson was throwing errors whenever I attempted to call the BayesianRidge model, preventing me from reproducing the issue. These errors included unsupported compiler arguments and warnings about mismatched debug and release builds.

After significant troubleshooting, I rebuilt scikit-learn using a modified approach, ensuring that meson was installed and configured correctly via wheel installation. I also resolved conflicts with dependencies like NumPy and Cython, meeting the minimum version requirements. With these adjustments, the build process completed successfully, and I was finally able to replicate the issue.

Here is the new scikit-learn build process that worked for me:

```bash
   1 python --version                                                                                                  
   2 python -m venv sklearn-env                                                                                        
   3 cd ..                                                                                                             
   4 cd ..                                                                                                             
   5 cd repos\                                                                                                         
   6 ls                                                                                                                
   7 cd Building_from_source\                                                                                          
   8 python -m venv sklearn-env                                                                                        
   9 .\sklearn-env\Scripts\activate                                                                                    
  10 ls                                                                                                                
  11 cd sklearn-env                                                                                                    
  12 ls                                                                                                                
  13 cd Scripts                                                                                                        
  14 ls                                                                                                                
  15 activate                                                                                                          
  16 source activate                                                                                                   
  17 cd ..                                                                                                             
  18 cd ..                                                                                                             
  19 Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned                                              
  20 sklearn-env\Scripts\activate                                                                                      
  21 pip install numpy scipy cython threadpoolctl joblib pytest                                                        
  22 pip install wheel numpy scipy cython meson-python ninja                                                           
  23 git clone https://github.com/sinhabintebabul/scikit-learn.git                                                     
  24 cd scikit-learn                                                                                                   
  25 git checkout main   git                                                                                              
  26 git pull                                                                                                          
  27 python setup.py build_ext --inplace                                                                               
  28 dir                                                                                                               
  29 pip install build meson-python                                                                                    
  30 python -m build --wheel                                                                                           
  31 ls                                                                                                                
  32 cd dist                                                                                                           
  33 ls                                                                                                                
  34 pip install scikit_learn-1.7.dev0-cp311-cp311-win_amd64.whl                                                       
  35 python -c "import sklearn; print(sklearn.__version__)"                                                       
```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Progress Expectations:
Now I am delving deep in the code of BayesianRidge Model and identifying the source of the issue. I aim to have a solution by the first half of this week.
