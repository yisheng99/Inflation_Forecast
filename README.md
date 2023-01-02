How to forecast inflation (consumer price index) using OLS?

Ordinary Least Square (OLS) is a statistical method that can be used to model the linear relationship between a dependent variable and one or more independent variables. 
 
In the context of forecasting inflation, the dependent variable would be the future inflation rate, and the independent variables could include factors that are thought to influence inflation.

I use Python to test this method on Malaysia's inflation. These are the steps I have taken to execute the the method:

Step 1. Import libraries (numpy, pandas, matplotlib) and data (historical Malaysia's inflation print, factors affecting Malaysia's inflation).
        For simpliticity sake, I have included only two factors - Unemployment and Money Supply.

Step 2. Plot a CPI graph to check the accuracy of the actual data - Whether the data reflects the actual Malaysia's CPI. (Chart 1)

Step 3. Create dataframe, add a constant term to the features to fit an intercept term in the model, and fit all the data into OLS model.

Step 4. Interpret the OLS results (Table 1), ie: is the R2 good? Significance of the factors? 

Step 5. Check for various assumptions, ie multicollinearity (Table 2), homoscedasticity (Chart 2), linearity (Chart 3, 4)

Step 6. Plot the actual and predicted values, compare to see whether the OLS model is a good forecast fit (Chart 5)


**CPI Graph**

Chart 1

![image](https://user-images.githubusercontent.com/121606452/210196185-8021547b-d739-44ea-aecf-2fb3c0a02505.png)


**OLS Result**

Table 1

![image](https://user-images.githubusercontent.com/121606452/210196436-8ba6572c-1d76-47ea-8a80-c4f23045a17c.png)


**Test for multicollinearity**

Table 2

![image](https://user-images.githubusercontent.com/121606452/210196446-70b677b8-773f-4162-9d4c-5e94dfa36691.png)


**Test for homoscedasticity**

Chart 2

![image](https://user-images.githubusercontent.com/121606452/210196156-5fda1075-f972-472c-a2e5-ed1a412542a2.png)

**Test for linearity**

Chart 3

![image](https://user-images.githubusercontent.com/121606452/210196170-373d5291-68f0-487a-b69c-f40ecb6232a2.png)

Chart 4

![image](https://user-images.githubusercontent.com/121606452/210196174-d2b7f8c2-ffcf-49e8-81d5-915658ec77f7.png)


**Test for model fit**

Chart 5

![image](https://user-images.githubusercontent.com/121606452/210196180-7665e64b-d9f6-49f8-8027-a30fc11a6a0e.png)


This is just a very simple example, and the result of the model is acceptable - good r2, factors are significant, low multicollinearity and good model fit.

This means that the model can explain the fluctuations in the consumer price index. Now, once we have established the accuracy of the model, we can proceed to make predictions for say, 12 months in the future. We could use the model to forecast inflation 12 months forward by inputting values for the independent variables that correspond to the expected values 12 months in the future, and using the model to predict the dependent variable (Consumer price index) at that point in time.


