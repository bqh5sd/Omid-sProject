# Regression-Module
The Regression Module is a Python package that takes inputs of molecular fingerprints or SMILES and outputs the performance of four regression models: Linear Regression, Gaussian Process Regression, Decision Tree Regression, and Random Forest Regression. The models' performance is quantitatively measured through statistics, specifically R^2, MSE, MAE, and R Pearson Correlation Coefficient values. 

# Dependencies:
**scikit-learn**: 1.2.1, py310hd77b12b_0
- from sklearn.linear_model import LinearRegression
- from sklearn.gaussian_process import GaussianProcessRegressor
- from sklearn.tree import DecisionTreeRegressor
- from sklearn.ensemble import RandomForestRegressor
- from sklearn.gaussian_process.kernels import RBF
- from sklearn.model_selection import train_test_split
- from sklearn.model_selection import GridSearchCV
- from sklearn.metrics import r2_score
- from sklearn.metrics import mean_squared_error
- from sklearn.metrics import mean_absolute_error

**pandas:** 1.5.3, py310h4ed8f06_0
- import pandas as pd
  
**numpy:** 1.23.5, py310h60c9a35_0
- import numpy as np
  
**time**

**datetime**

**sys**

**matplotlib:** 3.7.0, py310haa95532_0
- import matplotlib.pyplot as plt

**rdkit**: 2023.3.2, pypi_0
- from rdkit import Chem
- from rdkit.Chem import AllChem

# Organization
The project is organized into folders:
- Code contains the various versions of the Regression Metrics code, and is split into subfolders based on the inputs taken.
- data contains the data used to develop and analyze the model

# Code Versions:
I created multiple versions of both the fingerprint and SMILES versions of this code to create various run times. For larger data sets, the Regression_Metrics code can take multiple hours to run. Therefore, if a rough estimate is all the user requires, they can use the Fast_Regression_Metrics code in order to gain these results without waiting as long for results.

**Fast_Regression_Metrics:**
Optimization of the four regression models is removed from the code to give less accurate but faster results.

**Regession_Metrics:**
Some parameters are optimized, but for models that take longer to process (namely Gaussian Process Regression and Decision Tree Regression) only one or two parameters are optimized to prevent the code from running for excessive amounts of time.

**Slow_Regression_Metrics:**
In this version of the code, more optimized parameters are included, meaning the code will take longer to run but produce stronger results.

**Regression_Metrics_Graphs**
This version outputs the same statistics but also outputs graphs of each regression model's performance. On the x-axis are the values predicted by the model and on the y-axis are the true values.

# Datasets used to create model

**Lipophilicity:** The main dataset used to create this model was a Lipophilicity data set, included in the "Data" folder in this repository. I used both a fingerprint and SMILES version of this dataset to ensure that both versions of the code returned the same results. The Lipophilicity data set had fingerprints of length 1024 and 4200 rows of data.

**PDBBind:** I incorporated the PDBbind dataset to test my model after I developed it. This data set contains fingerprints of length 2048 and 9880 rows of data. This data set, because it was significantly larger, took significantly longer to run. Whereas the Gaussian model took 15 minutes to run for the Lipophilicity dataset, it took 3 hours to run with the PDBbind dataset. However, the model did continue to function properly.

**Contact:**
Steffanie Jones

djy6ge@virginia.edu
