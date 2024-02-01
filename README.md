# Derbyshire-Crime-Analysis-using-R

### Introduction

The aim of this project is to analyze the crime data set from different regions in Derbyshire. The objectives of this project are to: 

 - Gain a better understanding of the data set through descriptive visualizations 
 - Evaluate the relationship between variables in the data set using linear regression.


### Dataset Description
The provided dataset includes data on the number of criminal incidents that have been reported in various Lower Layer Super Output Areas (LSOAs) of Derbyshire. The dataset contains 642 observations and 18 variables. 

### Summary Statistics - Normality Distribution

Skewness is a measure used to fact check how the data deviates from a normal distribution (Gawali, 2021). The tail of the distributions as shown in the Density plot below are longer on the positive side which is indicative that the crime variables are positively skewed.


Figure 1: Density Plot of the Crime Data
![Density Plot](https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/3973f643-a97c-4955-8f43-863622c551e9)


This phenomena of the data led to the decision of log transforming the data. Log transformation is a method used to reduce the skewness of the data. It helps to achieve a much more closer bell curve as shown below (Htoon, 2020):

Figure 2: Density Plot of the Log Transformed Crime Data
![Log Transformed Density Plot](https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/a2d31d1c-68d0-406c-8749-8a41853bb5eb)

The skewness values for all variables are closer to zero indicating that the data is less skewed after log transformation. This suggests that the log transformation has assisted in reducing the degree of the asymmetry in the variable distribution. In contrast to the non-transformed data, where the highest positive skewness value for shoplifting was 2.39, the highest negative skewness value for other.theft is now only -0.03, down from -1.62. This shows that the skewness of the data for all variables has been significantly reduced by log transformation. Most of the variables' means are lower than their medians when compared to the first and third quartiles, which indicates that the distributions are negatively skewed. Furthermore, for many of the variables, the median tends to be closer to the 3rd quartile than the 1st quartile, indicating that the upper half of the data is more dispersed than the lower half.

### Simple Linear Regression
Examining the relationship between one independent and dependent variable is the key objective of linear regression analysis. Statistically, y= β0 + β1x+ε represents the relationship between one independent variable (x) and a dependent variable (y). The estimated value of y in this equation when x is equal to zero is denoted by the symbol β0, or the y intercept. The regression coefficient, which is denoted by the value of β1, indicates that there will be an expected increase in the dependent variable for each unit increase in the independent variable. The random error component symbol (ε), which denotes the imprecision of regression, shows that, in reality, no independent variable can accurately predict the change in any dependent variable (Ali and Younas, 2021). Below is the summary of the linear regressions models where population was used as an independent variable for each of the crime variable.


