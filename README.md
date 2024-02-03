# Derbyshire-Crime-Analysis-using-R

## Introduction

The aim of this project is to analyze the crime data set from different regions in Derbyshire. The objectives of this project are to: 

 - Gain a better understanding of the data set through descriptive visualizations 
 - Evaluate the relationship between variables in the data set using linear regression.


### Dataset Description
The provided dataset includes data on the number of criminal incidents that have been reported in various Lower Layer Super Output Areas (LSOAs) of Derbyshire. The dataset contains 642 observations and 18 variables. 

## EDA


<p align="center">
Figure 1: Total Population by City
 </p>
 
<p align="center">
 <img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/d941e0fa-bc4b-4c0c-9873-ea11526f0792" alt="Total Population by City">
</p>


<p align="center">
Figure 2: Total Crime by City
 </p>
 
<p align="center">
<img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/823e5e9d-e720-4ea2-b83b-24d651c78438" alt="Total Crime by City">
</p>


<p align="center">
Figure 2: Map Plot of Population Density
 </p>

<p align="center">
<img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/dfa8714d-84a4-4e3f-bb88-d7955905770b" alt="Map Plot of Population Density">
</p>


















## Linear Regression
### Summary Statistics - Normality Distribution

Skewness is a measure used to fact check how the data deviates from a normal distribution (Gawali, 2021). The tail of the distributions as shown in the Density plot below are longer on the positive side which is indicative that the crime variables are positively skewed.

<p align="center">
Figure 1: Density Plot of the Crime Data
 </p>

<p align="center">
  <img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/3973f643-a97c-4955-8f43-863622c551e9" alt="Density Plot">
</p>

 
This phenomena of the data led to the decision of log transforming the data. Log transformation is a method used to reduce the skewness of the data. It helps to achieve a much more closer bell curve as shown below (Htoon, 2020):


<p align="center">
Figure 2: Density Plot of the Log Transformed Crime Data
 </p>

<p align="center">
  <img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/a2d31d1c-68d0-406c-8749-8a41853bb5eb" alt="Log Transformed Density Plot">
</p>

 The log transformation has reduced the skewness of the variable distribution. The means are lower than their medians, indicating negative skewness. The upper half of the data is more dispersed than the lower half.


### Model Results
The positive slope coefficient (β1) for each crime type shows a correlation between population and crimes. The intercept for each model is negative, indicating that crime rates remain lower than the area's normal rate even with zero population. The models fit the data well with R-squared values ranging from 0.5972 to 0.8772, accounting for 59.72% to 87.72% of the variation in dependent variables.


| Crimes | β0 | β1 |Multiple R-squared | Adjusted R-squared |
| :--- |:---: |:---: |:---: |:---: |
| Anti- Social Behavior | -1.8251	 | 1.1483	 | 0.8271	 | 0.8269 |
| Burglary | -2.3017	| 1.0029	| 0.828	| 0.8278 |
| Robbery	| -3.1896	| 1.1490	| 0.8774	| 0.8772 |
| Vehicle crimes	| -2.3595	| 1.0246	| 0.8403	| 0.84 |
| Violent crimes	| -1.8708	| 1.1862	| 0.8532	| 0.853 |
| Shoplifting	| -2.9528	| 1.1448	| 0.5978	| 0.5972 |
| Criminal.Damage...Arson	| -2.3063	| 1.1246	| 0.8322	| 0.832 |
| Other theft	| -2.3096	| 1.0034	| 0.7592	| 0.7588 |
| Drugs	| -2.8459	| 1.0081	| 0.7824	| 0.782 |
| Other Crimes	| -3.159	| 1.144	| 0.8501	| 0.8499 |
| Bike theft	| -2.8323	| 1.0755	| 0.8301	| 0.8299 |
| Possession of Weapons	| -3.0845	| 1.0959	| 0.8685	| 0.8683 |
| Public order	| -2.5385	| 1.1412	| 0.7997	| 0.794 |
| Theft from the Person	| -3.1370	| 1.0746	| 0.8566	| 0.8564 |

#### Linearity: 
Linear regression assumes a linear relationship between the dependent and independent variables. If the relationship is nonlinear, using a linear regression model may produce unreliable results. For the models, the assumption of linearity holds.

<p align="center">
Figure 3: Linearity Plot of the Models
 </p>
 
<p align="center">
  <img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/c66a77a9-e7d8-46dd-a705-2cb468234b5f" alt="Linearity Plot">
</p>


#### Correlation:
The residuals are lowly correlated especially at the bottom left of the plot while the top right has stronger correlation between variables. Anti-social behaviour and Public Order have a correlation of 0.8. This is the same with the pairs of Anti-social behaviour and Violent Crimes, Anti-social behaviour, and Criminal Damage Arson

<p align="center">
Figure 4: Correlation Heatmap of Residuals
</p>

<p align="center">
  <img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/2ab95509-8163-4671-bbf0-f31a2838b00e" alt="Correlation Heatmap of Residuals">
</p>


#### Hierarchical Clustering:
A dendrogram is a diagram that shows the outcomes of hierarchical clustering. It helps sort related objects into clusters based on their similarity. The relationships between the clusters are shown graphically in the dendrogram. In Figure 5, the data is in 3 clusters colored red, green, and blue.
   
<p align="center">
 Figure 5: Cluster Dendogram
</p>


<p align="center">
  <img src="https://github.com/siraug/Derbyshire-Crime-Analysis-With-R/assets/122705182/1889be29-d13c-4c9d-854f-1da2c03b05a4" alt="Cluster Dendogram">
</p>




















