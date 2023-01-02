How to forecast inflation using OLS?

Ordinary Least Square (OLS) is a statistical method that can be used to model the linear relationship between a dependent variable and one or more independent variables. 
 
In the context of forecasting inflation, the dependent variable would be the future inflation rate, and the independent variables could include factors that are thought to influence inflation.

I use Python to test this method on Malaysia's inflation. These are the steps I have taken to execute the the method:

Step 1. Import libraries (numpy, pandas, matplotlib) and data (historical Malaysia's inflation print, factors affecting Malaysia's inflation).
        For simpliticity sake, I have included only two factors - Unemployment and Money Supply.

Step 2. Create dataframe and fit the data into OLS model. Calculate the residuals as well

Step 3. Check for various assumptions, ie multicollinearity, homoscedasticity, linearity

Step 4. Plot the actual and predicted values, compare to see whether the OLS model is a good forecast fit

![image](https://user-images.githubusercontent.com/121606452/210196185-8021547b-d739-44ea-aecf-2fb3c0a02505.png)


                           OLS Regression Results                            
==============================================================================
Dep. Variable:                    CPI   R-squared:                       0.903
Model:                            OLS   Adj. R-squared:                  0.902
Method:                 Least Squares   F-statistic:                     537.4
Date:                Mon, 02 Jan 2023   Prob (F-statistic):           4.48e-59
Time:                        12:14:23   Log-Likelihood:                -237.84
No. Observations:                 118   AIC:                             481.7
Df Residuals:                     115   BIC:                             490.0
Df Model:                           2                                         
Covariance Type:            nonrobust                                         
================================================================================
                   coef    std err          t      P>|t|      [0.025      0.975]
--------------------------------------------------------------------------------
Money_Supply  2.741e-05   1.17e-06     23.496      0.000    2.51e-05    2.97e-05
Unemployment    -0.0170      0.003     -6.404      0.000      -0.022      -0.012
const           78.2362      1.212     64.545      0.000      75.835      80.637
==============================================================================
Omnibus:                        7.524   Durbin-Watson:                   0.103
Prob(Omnibus):                  0.023   Jarque-Bera (JB):                7.906
Skew:                           0.616   Prob(JB):                       0.0192
Kurtosis:                       2.702   Cond. No.                     1.28e+07
==============================================================================

        feature        VIF
0  Money_Supply   3.113984
1  Unemployment   3.113984
2         const  51.227945

Test for homoscedasticity

![image](https://user-images.githubusercontent.com/121606452/210196156-5fda1075-f972-472c-a2e5-ed1a412542a2.png)

Test for linearity

![image](https://user-images.githubusercontent.com/121606452/210196170-373d5291-68f0-487a-b69c-f40ecb6232a2.png)

![image](https://user-images.githubusercontent.com/121606452/210196174-d2b7f8c2-ffcf-49e8-81d5-915658ec77f7.png)

Test for model fit

![image](https://user-images.githubusercontent.com/121606452/210196180-7665e64b-d9f6-49f8-8027-a30fc11a6a0e.png)




