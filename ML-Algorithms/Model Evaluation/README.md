# Regression Model Evaluation

## R Rquared

SSres = SUM(yi - yip)^2
SStot = SUM(yi - yavg)^2
R^2 = 1 - (SSres/SStot)

- R^2 ranges between [0, 1]
- As closer is R^2 to 1, better the model performance

## Adjusted R^2
**Problem in R^2**   
As the new variables are added, R^2 values would either  stay constant or increase in magnitude. This is because, on addition of new variable/ new coefficient, SSres is subject to increase (while SStot remains same) and hence R^2 would decrease.  
In the best case, on addition of new variable (even irrelevant variable) R^2 would remain same (when SSres = 0).  

Thus, 
    Adj R^2 = 1 - (1 - R^2)*((n-1)/(n-p-1))

where, 
    n = sample size/ total dependent variables
    p = number of regressors/ no. of independent variables/ *penalization factor*


