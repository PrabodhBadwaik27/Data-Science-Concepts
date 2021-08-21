# Random Forest Regression

**STPE 1:** Pick 'k' data points from Training set at random.
**STEP 2:** Build the Decision Tree associated to these 'k' data points.
**STEP 3:** Choose the 'Ntree' number of trees you want to build, and repeat STEPS 1 and 2.
**STEP 4:** For a new data point, make each one of your 'Ntree' trees predict the value of 'y'for the data points in the question and assign the new data point the average across all of the predicted 'y' values