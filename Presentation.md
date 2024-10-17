## **Introduction:**

In this project, we analyzed datasets regarding greenhouse gas emissions from cities in 2016 and 2017. 
Our goal was to understand trends and identify potential correlations between variables such as population, GDP, and temperature. We applied various data analysis and machine learning methods, including linear regression, multiple regression, polynomial regression, and clustering techniques like KMeans clustering.

**Garbage in, Garbage out**

* the concept of "Garbage in, Garbage out" (GIGO) strongly applies in our project. Although we cleaned the data by filling in missing values using the mean and mode, this basic approach likely introduced inaccuracies. These data issues led to suboptimal results in our models, such as the low R² values in both linear and multiple regression. This directly reflects how the quality of input data affects the overall outcomes, making GIGO a key factor in our results

**Data Collection and Preprocessing:** 
The datasets we used had a significant amount of missing data and varying data quality, so we had to clean and fill in the missing values. 
We used the mean for numerical values and the mode for categorical variables. This was an effective approach, but  maybe could have been done better with other methods.

**Data Analysis:** 
We began with a basic analysis of the datasets. Here are some key points:

We explored the correlation between variables like population and total CO2 emissions, where we found a correlation of 0.73. This indicated that larger cities tend to have higher emissions, which makes sense.

Another correlation we discovered was between Scope 1 and Scope 2 emissions, which were strongly related to each other (correlation of 0.98). This shows that direct and indirect emissions from cities are closely linked.

**Challenges in the Analysis:** 
While we identified some interesting correlations, there were also several challenges:

Categorical variable “C40”: We found a negative correlation between this variable and population, suggesting that cities in the C40 initiative generally have lower emissions per capita. However, this conclusion is somewhat limited due to missing data in our dataset.

* Improvement Suggestion: It would have been beneficial to include more cities participating in C40 to achieve a more accurate analysis. We could have searched for more comprehensive datasets or alternative sources.

## **Modeling:**

**Linear Regression:** 

We started with a simple linear regression between population and total emissions. The model gave an R² value of 0.45, which means that about 45% of the variation in emissions could be explained by population size.

* Improvement Suggestion: We could have explored additional factors, such as energy consumption, transportation, or industrial activities, to improve the model’s accuracy.

**Multiple Regression:** 

We used both population and GDP as independent variables, but the model performed worse with an R² of 0.21. This suggests that GDP did not significantly contribute to explaining emissions.

* Improvement Suggestion: We could have added more variables, such as energy consumption or urbanization rate, to enhance the model’s performance.

**Polynomial Regression:** 

We applied polynomial regression to capture non-linear relationships between population and emissions, which yielded an R² of 0.56. However, we identified signs of overfitting, suggesting that the model might be too complex and fitting noise rather than meaningful patterns.

* Improvement Suggestion: To avoid overfitting, we could have used cross-validation to better assess the model's ability to generalize.

## **KMeans Clustering:**

* To determine the optimal number of clusters (K), we tested various values of K using both the Elbow method and Silhouette score:

* **The Elbow method** indicated a potential inflection point at 3 clusters, suggesting that 3 could be a good choice, as adding more clusters did not significantly reduce the distortion.

* However, when we evaluated the Silhouette score, we noticed that while 3 clusters gave the highest silhouette score, it also produced negative values for some data points, indicating that certain cities were incorrectly assigned to the wrong cluster.

* After further analysis, we decided that using 2 clusters was the better option. With 2 clusters, the Silhouette score was still high, and all data points had positive silhouette values, meaning the cities were more appropriately grouped within their clusters.

### Critical Assessment of Results:

* Although 2 clusters was the best choice based on our analysis, one critical point must be addressed: the clusters were unevenly sized. This imbalance suggests that the features we chose (emissions, population, GDP, and temperature) may not have been optimal for creating well-distributed clusters.

* Argument for feature selection: The features we selected, such as emissions data, population size, GDP, and temperature, are all relevant indicators of a city’s contribution to climate change and its economic activity. Thus, they seemed like logical choices for the clustering analysis.
  
* Critique of feature selection: However, the uneven cluster sizes indicate that certain cities may have been grouped together with very different cities. This could be due to skewed data or the over-dominance of one or two features (e.g., population or emissions levels). It’s also possible that including additional variables like energy consumption or transportation habits could have improved the clustering outcome.

### Areas for Improvement:

To address the issues we encountered, we could consider the following improvements:

* **Experiment with additional features:** Adding variables such as energy sources, transportation data, or industrial activities could help achieve better-distributed clusters and offer more insightful groupings.
  
* **Feature weighting and normalization:** We could explore the effect of applying different weights to certain features to avoid having one feature (like population) dominate the clustering results.

### Conclusion:

* Although using 2 clusters in KMeans was a reasonable choice based on our analysis and prevented negative silhouette values, there is still room for improvement in both the selection of features and the evaluation of the cluster structure. Future improvements in these areas would help us achieve a more nuanced understanding of how cities group together in terms of their environmental and economic impact.


## **Why Classification Makes Sense:** 

It would also make sense to apply classification in this project, as it could help categorize cities based on their emissions levels (e.g., high, medium, low) or GDP per capita. By using features like population, GDP, and total emissions, we can predict which class a city might fall into. Classification techniques such as decision trees or Naïve Bayes could further help distinguish between cities that meet or exceed environmental targets, aiding in better understanding city performance regarding emissions.

## **Overall Conclusion:** 

Our analysis has provided insights into how population and GDP impact cities' greenhouse gas emissions, but the accuracy of our models has been limited. We identified areas where more comprehensive data and alternative modeling techniques could improve the results. If we were to repeat the project, we would focus on including more relevant factors and employing more advanced methods to handle missing data and prevent overfitting.
