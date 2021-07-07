# Linear Regression

## Assumptions of Linear Regression

1. Linearity  
2. Homoscedasticity  
3. Multivariate Normality  
4. Independence of Errors  
5. Lack of Multicollinearity  

### Dummy Variables
**Dummy Variables** are the columns which are newly created for every value present in the *categorical variables* in dataset.

***Dummy Variable Trap***  
Always omit one dummy variable for every categorical variable.

## Methods of Building Models

1. ***All-in***
ML model built by considering *all the variables* present in datasets.

2. ***Backward Elimination***
Iterative approach of building a regression model such that the insignificant variables present in the dataset are eliminated from input parameters one-by-one with each iteration.

**Steps in Backward Elimination:**
- **STEP 1:** Select a threshold significance level to consider input for the model (usually SL = 0.05)
- **STEP 2:** Fit the model with all possible predictors
- **STEP 3:** Consider the predictor with the *highest p-value*.  
If p > SL, go to *STEP 4*
Else, *FINISH*
- **STEP 4:** Remove the predictor
- **STEP 5:** Re-fit model with remaining variables.
- **FINISH:** Your model is ready

3. ***Forward Selection***
4. ***Bidirectional Elimination***
5. ***Score Comparison***

***Note:***  
Types 2, 3 and 4 are alternatively referred as **Stepwise Regression**.