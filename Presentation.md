## **Introduction:**

In this project, we analyzed datasets regarding greenhouse gas emissions from cities in 2016 and 2017. 
Our goal was to understand trends and identify potential correlations between variables such as population, GDP, and temperature. We applied various data analysis and machine learning methods, including linear regression, multiple regression, polynomial regression, and clustering techniques like KMeans clustering.

## **Data Collection and Preprocessing:** 

The data had several missing values across both Quantitative(numerical) and Qualitative(categorical) data fields, which we addressed by applying appropriate methods:

* Numerical columns (e.g., Population, Emissions): Missing values were filled using the mean, ensuring consistency across the dataset without skewing the distribution.
* Categorical columns (e.g., City, Country): Missing values were replaced with the mode, which allowed us to maintain logical groupings for qualitative data.

* Additiontly, we also dropped some columns that we knew we didn't need like our location columns.

## **Data Analysis:** 
We began with a basic analysis of the datasets. Here are some key points:

We explored the correlation between variables like population and total CO2 emissions, where we found a correlation of 0.73. This indicated that larger cities tend to have higher emissions, which makes sense.

Another correlation we discovered was between Scope 1 and Scope 2 emissions, which were strongly related to each other (correlation of 0.98). This shows that direct and indirect emissions from cities are closely linked.

**Challenges in the Analysis:** 
While we identified some interesting correlations, there were also several challenges:

Categorical variable “C40”: The negative correlation suggests that larger cities (with higher populations) are less represented in the C40 group compared to smaller or medium-sized cities. Larger cities may face greater challenges in managing emissions due to their size and complexity, making it harder to meet the requirements of C40.

## **KMeans Clustering:**

* To determine the optimal number of clusters (K), we tested various values of K using both the Elbow method and Silhouette score:

* **The Elbow method** In the graph, we see that the distortion decreases rapidly from K=2 to K=4, but after that, it begins to decrease more slowly. This suggests that K=4 could be a good choice. However it only takes distortions into consideration and not for ex. Cluster quality and shape

* **Silhouette score** However, when we evaluated the Silhouette score, we noticed that while 3 clusters gave the highest silhouette score, it also produced negative values for some data points, indicating that certain cities were incorrectly assigned to the wrong cluster.

* After further analysis, we decided that using 2 clusters was the better option. With 2 clusters, the Silhouette score was still high, and all data points had positive silhouette values, meaning the cities were more appropriately grouped within their clusters.

### Critical Assessment of Results:

* Although 2 clusters was the best choice based on our analysis, one critical point must be addressed: the clusters were unevenly sized. This imbalance suggests that the features we chose (emissions, population, GDP, and temperature) may not have been optimal for creating well-distributed clusters.
  
* Critique of feature selection: However, the uneven cluster sizes indicate that certain cities may have been grouped together with very different cities. This could be due to skewed data or the over-dominance of one or two features (e.g., population or emissions levels). It’s also possible that including additional variables like energy consumption or transportation habits could have improved the clustering outcome or used normalization like Z-score normalization.

### Areas for Improvement:

To address the issues we encountered, we could consider the following improvements:

* **Experiment with additional features:** Adding variables such as energy sources, transportation data, or industrial activities could help achieve better-distributed clusters and offer more insightful groupings.
  
* **Feature weighting and normalization:** We could explore the effect of applying different weights to certain features to avoid having one feature (like population) dominate the clustering results.

## **Modeling:**

**Linear Regression:** 

We started with a simple linear regression between population and total emissions. The model gave an R² value of 0.45, which means that about 45% of the variation in emissions could be explained by population size.

* Choosing 80% of data for testing and only 20% for training is unusual in linear regression and can lead to unreliable results. Models need enough data to learn patterns, so it’s better to use a standard split like 70% training / 30% testing or 80% training / 20% testing for better generalization. If you test on too much data, metrics like R-squared might look good, but the model may not have learned properly. Which could be the reason for high MSE and RMSE.

**MAE (Mean Absolute Error) - 0.393:**

* Shows the average difference between predicted and actual values. In this case, the model is off by 0.393 units on average.

**MSE (Mean Squared Error) - 0.511:**

* Measures the average squared differences between predicted and actual values. It gives more weight to larger errors. Lower is better.

**RMSE (Root Mean Squared Error) - 0.715:**

* Similar to MSE, but it takes the square root to return the error to the original units. It shows that the typical prediction error is 0.715 units.

**R-Squared (R²) - 0.458:**

* Indicates how well the model fits the data. R² of 0.458 means the model explains 45.8% of the variance in the data. Closer to 1 is better.

## 

**Multiple Regression:** 

We used both population and GDP as independent variables, but the model performed worse with an R² of 0.21. This suggests that GDP did not significantly contribute to explaining emissions.

* Improvement Suggestion: We could have added more variables, such as energy consumption or urbanization rate, to enhance the model’s performance.

**Polynomial Regression:** 

We applied polynomial regression to capture non-linear relationships between population and emissions, which yielded an R² of 0.56. However, we identified signs of overfitting, suggesting that the model might be too complex and fitting noise rather than meaningful patterns.

**Signs of overfitting:** The curve is bending sharply to follow some data points, which could be an indication that the model is focusing too much on specific points instead of generalizing well

* Improvement Suggestion: To avoid overfitting, we could have used cross-validation to better assess the model's ability to generalize.


## **Why Classification Makes Sense:** 

It would also make sense to apply classification in this project, as it could help categorize cities based on their emissions levels (e.g., high, medium, low) or GDP per capita. By using features like population, GDP, and total emissions, we can predict which class a city might fall into. Classification techniques such as decision trees or Naïve Bayes could further help distinguish between cities that meet or exceed environmental targets, aiding in better understanding city performance regarding emissions.

## **Garbage in, Garbage out**

* the concept of "Garbage in, Garbage out" (GIGO) strongly applies in our project. Although we cleaned the data by filling in missing values using the mean and mode, this basic approach likely introduced inaccuracies. These data issues led to suboptimal results in our models, such as the low R² values in both linear and multiple regression. This directly reflects how the quality of input data affects the overall outcomes, making GIGO a key factor in our results

## **Overall Conclusion:** 

Our analysis has provided insights into how population and GDP impact cities' greenhouse gas emissions, but the accuracy of our models has been limited. We identified areas where more comprehensive data and alternative modeling techniques could improve the results. If we were to repeat the project, we would focus on including more relevant factors and employing more advanced methods to handle missing data and prevent overfitting.
