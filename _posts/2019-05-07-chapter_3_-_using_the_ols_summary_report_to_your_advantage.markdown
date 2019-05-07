---
layout: post
title:      "Chapter 3 - Using the OLS Summary Report to Your Advantage"
date:       2019-05-07 15:36:21 +0000
permalink:  chapter_3_-_using_the_ols_summary_report_to_your_advantage
---

Linear regression (AKA Ordinary Least-Squares or OLS regression) is a commonly used approach to clarify many of today’s complex affairs.

### What is OLS regression?

<em> Note: I will be demonstrating a multiple linear regression as our example using the DataSet “House Sales in King County, USA” from Kaggle.com, and which was manipulated by me in this [GitHub hyperlink](https://github.com/beverlyfdelarosa/dsc-1-final-project-online-ds-sp-000/blob/master/student.ipynb). </em>

OLS regression is a statistical technique where we try to estimate the dependent variable (y_hat) with a given set of independent variables separated into a constant coefficient/y-intercept (β_0 ), the known independent variables coefficients attached to its slope (β_1(x_1) + β_2(x_2) + ⋯ + β_n(x_n)), and the error that balances the random noise (ε). When a good predictive model uses a fitted line to best describe the relationship between the actual observations, we can confidently predict future observations.

 y_hat = β_0 + β_1(x_1) + β_2(x_2) + ⋯ + β_n(x_n) + ε

Example: Predicting a house’s price based on its features, such as the square footage of the lot or living space, or distance from parks and schools.

### What consists of a good DataFrame?

Often in real life, DataFrames (a DataSet organized into named columns- think of it like a table with headers) are huge in shape (rows X columns) and involve several layers to monitor. To best control the results to be non-biased, there are several factors to make sure your DataFrame complies with.



1.	Assume the relationship to be linear between the dependent variable (DV)  and independent variables (IVs). <br>
&nbsp;&nbsp; a.	Error terms/Residuals are normally distributed with a mean of 0. <br>
&nbsp;&nbsp; b.  Error terms/Residuals have a constant variance showing that there is no heteroscedasticity.
2.	The DV is continuous in nature.
3.	No multicollinearity among the IVs.
4.	No outliers are present in our data.

### Breaking down our assumptions.

<strong> 1. Because regression is a “parametric” technique, the linearity assumption satisfies the premise that a change in our predictors/IVs will affect the target/DV. </strong><br>

a.	The normality assumption allows us to be confident in our hypothesis testing. Although performing OLS isn’t necessary for predicting estimates, it could be a good idea to standardize your data anyhow in order to allow you to do further testing on specifics. The “Principle of Least Squares” tells us that a model should have a minimal deviation difference between an actual value and the line of best fit, so a mean of 0 indicates that both positive and negative errors cancel each other out. If you are using the OLS summary chart, the Jarque-Bera (JB) is a good place to check. A probability of p < 0.05 means that the result is significant and the is a violation of normality.  <br>

b.  The homoscedastic assumption determines whether a regression model’s ability to predict a DV is consistent across all values of that DV. When the residuals are equal across the regression line, we can trust that the accuracy of the model. If you are using the OLS summary chart, the “F-statistic” is a good place to check. A probability of p < 0.05 means that the result is significant and the variance is constant.

<strong> 2.	OLS works only with continuous numerical data, but what if we have categorical IVs? </strong>

Transforming appropriate IVs to categories eliminates the possibility that the IVs’ values are continuous when instead they are discrete. When we use on-hot encoding to create these dummy variables, we are still able to use a single regression equation to represent all the smaller sub-groups. However, it is a balance between accuracy and computational accuracy.

There is no penalty for having 100s of dummies on your analysis, but it is important to realize that because this step can quickly expand your DataFrame’s shape, it thus requires more computational power. There’s no exact work-around for this, but there are several methods to deal with these variables. These techniques are more advanced than the linear regression process, so you may have to play around with your data before to get what you’re looking for.
* By multilevel/hierarchical modeling and/or combining levels, we account for the correlations among the observations within each group and allow for separate best fitted lines to be estimated with less impact from rare or redundant levels. 
* By converting our data type to a number, we may decrease the performance of the model since the overlapping of certain IVs are unlikely to happen and can get treated similarly to multiple levels of non-numeric IVs.
* By undergoing feature selection, our data type to a number, we reduce our number of IVs to the ones that have more impact on our model and remove the ones that can lead to noise and misdirection. 


<strong> 3.	If my IVs are highly correlated with each other, then the estimates of my standard error of regression coefficients will make some IVs statistically insignificant when they should be significant. </strong>

You are wanting as much variability in your model as possible, so you are wanting to toss categorical or ordinal variables that are strongly associated. Using a correlation matrix or heat map if there are many IVs can show you which data you should drop due to redundancy. If you are using the OLS summary chart, the “Cond. No.” (condition number) is a good place to check. Oftentimes if it’s too large, a warning will be raised that multicollinearity among the IVs are detected.

<strong> 4.	No outliers are present in our data. </strong>

The “Coefficient of Determination” (R-squared) gives us a suggested proportion of variation in the DV which can be explained by the IVs. Mathematically, it is the ratio of predicted and observed values. A perfect fit gives us R-squared = 1, and a poor fit gives us R-squared = 0.

Sometimes not all the IVs will have a significant weight to predicting the DV, but as new ones are added to the model, they will still increase the R-squared value regardless. So instead, it is better to use the adjusted R-squared value to compensate for the magnitude that the IVs add and thus will always be a smaller number than the regular R-squared.

A general rule of thumb is if the adjusted R-squared value increases when a new IV is added to the model, the IV should remain in the model. If the adjusted R square decreases when the new IV is added, then the IV should not remain in the model.

### Example: Running an OLS regression multiple times until I get a good predictive model.

Figure 1 – Scatterplots of our IVs against the DV Price

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/V7lYtaV"><a href="//imgur.com/V7lYtaV"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/TIcMFZh.png)
</center>

Figure 2 – OLS Regression results of Run 1 including the top left providing basic information about the model fit, top right telling us our goodness of fit, the middle section of the coefficients omitted, and the bottom table which performs several statistical tests to assess the distribution of the residuals.

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/V7lYtaV"><a href="//imgur.com/V7lYtaV"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/MbpBSWf.png)
</center>

Figure 3  – OLS Regression results of Run 2 including the top left providing basic information about the model fit, top right telling us our goodness of fit, the middle section of the coefficients omitted, and the bottom table which performs several statistical tests to assess the distribution of the residuals.

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/V7lYtaV"><a href="//imgur.com/V7lYtaV"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/irF2FNN.png)
</center>

<strong> Run 1:  After filtering and standardizing our data then expanding to 220 predictors. </strong>

1.	We saw in our scatterplots (Figure 1) that positive linear relationships are noticeable for both our continuous and discrete IVs. <br><br>
a.	Our “JB” test (Figure 2) has a significant p-value (<0.05), so our model’s residuals are not normally distributed. This isn’t necessary when it comes to predicting an estimate (of price), but we could further tweak our transformations in order to do other statistical testing (e.g., hypothesis).  <br><br>
b.	Our “F-Statistic” test (Figure 2) has a significant p-value (<0.05), which tells us that our variance is constant. This allows us to assume our model fits homoscedasticity.
2.	Our DV, Price, is continuous (Figure 1).
3.	Our “Cond. No” (Figure 2) is large, which suggests that there may be strong multicollinearity or other numerical problems.
4.	Because our R-squared and Adjusted R-Squared (Figure 2) are the same, we know that our features are significant in the model, and thus do not have many outliers. But because of multicollinearity, our accuracy goes down and not within an appropriate range of [0, 1].

<strong> Run 2:  After RFE reduced our significant predictors to 166. An alpha set to .005 further eliminates the not as significant features. Furthermore, using a low bias, high variance number of cross validations, we see that despite their added complexity, our model represents a large noise component in their training set, making their predictions less accurate. </strong>
1.	We would still have a positive linear relationship as shown in our scatterplots (Figure 1), but more outliers would be trimmed. <br><br>
a.	Similar reasoning to previous run. We can trust our results though because we see that our test and training root mean absolute error are very similar showing that the test wasn’t overfitted or underfitted. <br><br>
b.	Our “F-Statistic” test (Figure 3) still has a significant p-value (<0.05). When we further apply our test to our top categorical features using the the Goldfeld-Quandt (GQ) test, our p-values are not significant (> 0.05), meaning we do not have evidence of heteroskedasticity.
2.	Our DV, Price, is still continuous (Figure 1).
3.	Our “Cond. No” (Figure 3) went from several thousands to a couple hundreds, eliminating our warning from multicollinearity.
4.	Again, our R-squared and Adjusted R-Squared (Figure 3) are the same, but our model accuracy is now within its appropriate range.


