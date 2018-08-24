# Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis #
## Performance comparison of self-coded Stochastic Gradient Descent vs Sklearn OLS vs Batch Gradient Descent ##

### Objective: ###

1. **To implement Stochastic Gradient Descent (SGD)** based on how the gradient descent logic works, to minimize the cost so as to find the best fit.

2. Compare and analyse the difference in outcome between **self implementation of SGD vs sklearn’s Ordinary Least Squares (OLS)** implementation. You may use graphical plots to do the same.

3. **Implement Batch Gradient Descent** to compare the outcome: **both timing as well as data**.

### At a glance ###

1. **Stochastic Gradient Descent (SGD)** is implemented and cost analysis has been down for every 100 iterations. It **has been tested for different batch sizes & iterations, to find out difference in RMSE, graphically depicted using scatter plots**. The formulas used in SGD implementation is given in the report below.

2. **Sklearn’s Ordinary Least Squares (OLS) is used on the same dataset and timing and error evaluation has been done** for head to head comparison. **Batch Gradient Descent algorithm** is also implemented for comparison.

3. The **timing comparison of all the 4 methods:** Batch Gradient Descent, Stochastic GD, low K SGD and Sklearn’s OLS has been done. The **PDF of errors is plotted with kdeplot** to identify the deviation of distribution from actual target value distribution. **The summary of results and conclusion is provided at the end of the report.**

### Data Source: ###

Boston Dataset from Sklearn Datasets.

### Dataset Details on Boston House Prices ###

***Characteristics:***

Number of Instances: 506
Number of Attributes: 13 numeric/categorical predictive
Median Value (attribute 14) is usually the target

***Attribute Information (in order):***

- CRIM per capita crime rate by town
- ZN proportion of residential land zoned for lots over 25,000 sq.ft.
- INDUS proportion of non-retail business acres per town
- CHAS Charles River dummy variable (= 1 if tract bounds river; 0 otherwise)
- NOX nitric oxides concentration (parts per 10 million)
- RM average number of rooms per dwelling
- AGE proportion of owner-occupied units built prior to 1940
- DIS weighted distances to five Boston employment centres
- RAD index of accessibility to radial highways
- TAX full-value property-tax rate per $10,000
- PTRATIO pupil-teacher ratio by town
- B 1000(Bk - 0.63)ˆ2 where Bk is the proportion of blacks by town
- LSTAT % lower status of the population
- MEDV Median value of owner-occupied homes in $1000's

***Missing Attribute Values:*** None

***Creator: Harrison, D. and Rubinfeld, D.L.***

This is a copy of UCI ML housing dataset.
http://archive.ics.uci.edu/ml/datasets/Housing

This dataset was taken from the StatLib library which is maintained at Carnegie Mellon University. The Boston house-price data of Harrison, D. and Rubinfeld, D.L. 'Hedonic prices and the demand for clean air', J. Environ. Economics & Management, vol.5, 81-102, 1978. Used in Belsley, Kuh & Welsch, 'Regression diagnostics ...', Wiley, 1980. N.B. Various transformations are used in the table on pages 244-261 of the latter. The Boston house-price data has been used in many machine learning papers that address regression problems.

***References***
- Belsley, Kuh & Welsch, 'Regression diagnostics: Identifying Influential Data and Sources of 
- Quinlan,R. (1993). Combining Instance-Based and Model-Based Learning. In Proceedings on the 
- many more! (see http://archive.ics.uci.edu/ml/datasets/Housing)

### Hand Coding of Stochastic Gradient Descent ###

The error is calculated using the below formula at every iteration. The derivative term, w.r.t. w and b has to be negated on every iteration. Derivate is calculated using this formula at every iteration.

Then we negate the parameter gradient from each parameter, adjusted by learning rate. We use this formula, params = params - learning rate * params_gradient.

**Low K, Stochastic Gradient Descent: Cost Analysis** <br/>
Cost of iteration #100 = 72.81 <br/>
Cost of iteration #200 = 59.0 <br/>
Cost of iteration #300 = 159.28 <br/>
Cost of iteration #400 = 17.85 <br/>
Cost of iteration #500 = 1934.25 <br/>
Cost of iteration #600 = 30.67 <br/>
Cost of iteration #700 = 394.6 <br/>
Cost of iteration #800 = 575.87 <br/>
Cost of iteration #900 = 11.97 <br/>
Cost of iteration #1000 = 98.75 <br/>
Cost of iteration #1100 = 190.68 <br/>
Cost of iteration #1200 = 13.14 <br/>
Cost of iteration #1300 = 7.5 <br/>
Cost of iteration #1400 = 85.12 <br/>
Cost of iteration #1500 = 49.15 <br/>
Cost of iteration #1600 = 54.78 <br/>
Cost of iteration #1700 = 10.78 <br/>
Cost of iteration #1800 = 10.68 <br/>
Cost of iteration #1900 = 30.55 <br/>
Cost of iteration #2000 = 123.18 <br/>

**Stochastic Gradient Descent: Cost Analysis** <br/>
Cost of iteration #100 = 14.76 <br/>
Cost of iteration #200 = 52.03 <br/>
Cost of iteration #300 = 232.23 <br/>
Cost of iteration #400 = 31.24 <br/>
Cost of iteration #500 = 15.02 <br/>
Cost of iteration #600 = 4.38 <br/>
Cost of iteration #700 = 24.46 <br/>
Cost of iteration #800 = 22.23 <br/>
Cost of iteration #900 = 9.26 <br/>
Cost of iteration #1000 = 7.12 <br/>

**Batch Gradient Descent: Cost Analysis** <br/>
Iteration #100 Cost = 19.69 <br/>
Iteration #200 Cost = 19.56 <br/>
Iteration #300 Cost = 19.55 <br/>
Iteration #400 Cost = 19.55 <br/>
Iteration #500 Cost = 19.55 <br/>
Iteration #600 Cost = 19.55 <br/>
Iteration #700 Cost = 19.55 <br/>
Iteration #800 Cost = 19.55 <br/>
Iteration #900 Cost = 19.55 <br/>
Iteration #1000 Cost = 19.55 <br/>

RMSE LowK SGD = 11.1 <br/>
RMSE of SGD   = 2.67 <br/>
RMSE of GD    = 4.42 <br/>

***Percentage change in Weight Vectors from GD to SGD = 0.2% ***

![hc1](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/hc1.PNG)

![hc2](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/hc2.PNG)

![hc3](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/hc3.PNG)

### Linear Regression using Sklearn’s OLS ###

RMSE = 5.31

![ols](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/ols.PNG)

### Timing Comparison of SGD, Batch GD, SKlearn & Low K SGD ###

Time Taken by Low K SGD is 1.68 seconds when k = 5 <br/>
Time Taken by SGD is 1.75 seconds when k = 10 <br/>
Time Taken by Batch GD is 1.96 seconds when k = 339 <br/>
Time Taken by Sklearn OLS is 0.0 seconds <br/>

### Error Comparison of SGD, Batch GD & Sklearn’s OLS ###

![pdf_ols](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/pdf_ols.PNG)

![pdf_gd](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/pdf_gd.PNG)

![pdf_pv](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/pdf_pv.PNG)

### Summary ###

![summary](https://github.com/AdroitAnandAI/Hand-coded-SGD-vs-Sklearn-OLS-vs-Batch-Gradient-Descent-Analysis/blob/master/images/summary.PNG)

### Conclusion ###

1. **RMSE of Stochastic Gradient Descent is found to be the lowest** compared to other algorithms. The RMSE value would fluctuate a bit because the algorithm is inherently stochastic. But, the low RMSE values signify the method is working fine.

2. **RMSE of SGD < Batch GD < Sklearn’s OLS < Low K SGD**. The low batch size increases the error value significantly.

3. **Timing of Sklearn’s OLS is great but the RMSE value is higher. There is significant reduction in time, when we do Stochastic GD instead of Batch GD.**

4. The **scatter plot of Low K SGD is more perturbed than SGD scatter plot**. SGD plot is more linear which signifies less deviation/ error.

5. When k is low (we have taken k= 5), then the minimized MSE is found to be high. But when we increase iterations, the minimum cost moves towards optimum. Hence, **for lower K, iterations should be more**. 

6. The **PDF** of errors in Sklearn’s OLS are centered around 0. From the plot, it is noticed that there are more errors on the -ve side. To improve the solution, we have to reduce the errors on the -ve side.

7. The PDF of predicted values are centered around 20. **As the error PDF is much to the left of predicted PDF, it is found that the % of errors is acceptable**.

8. The PDF of errors of Batch Gradient Descent is similar to the Sklearn’s OLS method. Hence, the error in fit should be almost same. However, **the PDF error plot of SGD implementation is way off on the negative side, hence errors are more**.

9. The error distribution kdeplot of SGD implementation would become near to Sklean’s method when the batch size(k) of SGD  implementation increases. As we take more points in each iteration, the approximation error would reduce, though it would take more time.
