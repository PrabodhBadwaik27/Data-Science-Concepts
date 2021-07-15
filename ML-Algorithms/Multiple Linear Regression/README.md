# Multiple Linear Regression

## Assumptions of Linear Regression (OLS Assumptions)

1. ***Linearity***
2. ***No Endogeneity***
3. ***Normality & Homoscedasticity***
4. ***No Autocorrelation***
5. ***No Multicollinearity***

**Note:**  
ML Engineer doesn't necessarily need to validate the OLS assumptions on a new dataset before model training.  
The reason is, after model training if the Linear Regression model yields less poor accuracy than other algorithms, then anyhow the model will be scraped out.  

[Reference](https://365datascience.com/tutorials/statistics-tutorials/ols-assumptions/)

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
**Dummy Variable Trap** (concept) suggests to necessarily omit one dummy variable for every categorical variable since conceptually it's redundant to have a dummy variable for all the categorical variables.

3. As stated before in regards of OLS assumptions, ML Engineer doesn't necessarily need to take any additional steps for **avoiding dummy variable trap** and **Model building type** for model training.  
The reason is, the SciKit-Learn library itself takes care of both the aspects.  