# Linear Regression

## Assumptions of Linear Regression (OLS Assumptions)

1. ***Linearity***  
Data points must be linear.
If the data is not linear, transform it accordingly.

2. ***Homoscedasticity & Normality***
Uneven spread of data points around the regression line

3. ***Multivariate Normality***

4. ***No Endogeneity/ Independence of Errors***
No correlation between error and independent variables

5. ***Lack of Multicollinearity***
Two or more variables have high correlation

6. ***No Autocorrelation***
No serial correlation

## Methods of Building Models

1. ***All-in***   
ML model built by considering *all the variables* present in datasets.

2. ***Backward Elimination***  
Iterative approach of building a regression model such that the insignificant variables present in the dataset are eliminated from input parameters one-by-one with each iteration.

    - **Steps in Backward Elimination:**
        - **STEP 1:** Select a threshold significance level to consider input for the model (usually SL = 0.05)
        - **STEP 2:** Fit the model with all possible predictors
        - **STEP 3:** Consider the predictor with the *highest p-value*.    
        If p > SL, go to *STEP 4*  
        Else, *FINISH*  
        - **STEP 4:** Remove the predictor
        - **STEP 5:** Re-fit model with remaining variables.
        - **FINISH:** Your model is ready

3. ***Forward Selection***     
Iterative approach of building a regression model such that a single significant variable is added in fitting at every iteration.

    - **Steps in Forward Selection:**
        - **STEP 1:** Select a significance level to enter the model (usually SL = 0.05)
        - **STEP 2:** Fit all the simple regression models y ~ x(n).  
        Select the one with lowest p-value.
        - **STEP 3:** Keep this variable and fit all possible models with extra one predictor added to the one(s) you already have.
        - **STEP 4:** Consider the predictor with the *lowest* p-value.  
        If p < SL, go to *STEP 4*    
        Else, *FINISH*  
        - **FINISH:** Keep the *previous* model 

4. ***Bidirectional Elimination***
    - **Steps in Bidirectional Elimination:**
        - **STEP 1:** Select a significance level to enter (SLENTER) and to stay (SLSTAY) in the model.
        (usually, SLENTER = 0.05, SLSTAY = 0.05)
        - **STEP 2:** Perform the *STEP 2* of *Forward Selection Method* considering *p < SL = SLENTER* to enter
        - **STEP 3:** Perform *ALL* steps of *Backward Elimination, p < SL = SLSTAY* to stay
        - **STEP 4:** Repeat *STEP 2* and *STEP 3* till no more variable can enter and exit
        - **FINISH:** Your model is ready

5. ***Score Comparison***  
**Score comparison** model can be described as *selecting the best* model from *all possible models*.
    - **Steps in Score Comparison method:**
        - **STEP 1:** Select a criterion of godness of fit (e.g. Akaike criterion)
        - **STEP 2:** Construct all possible regression models   
        Total combinations = (2^N - 1)   
        where, N is no. of variables  
        **STEP 3:** Select the one with best criterion (score)
        **FINISH:** Your model is ready

    - **Drawbacks of Score Comparison method**
        - Non-feasible method, both resource and time cosuming.
        - No scope of human interference, thus difficult to interprete 

***Notes:***  
1. Types 2, 3 and 4 are alternatively referred as **Stepwise Regression**.

2. ***Dummy Variables***
**Dummy Variables** are the columns which are newly created for every value present in the *categorical variables* in dataset.
**Dummy Variable Trap** (concept) suggests to necessarily omit one dummy variable for every categorical variable.