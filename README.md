# Comparing Classifiers
Practical Application Assignment 17.1
# Practical Application Assignment 17.1: Comparing Classifiers
 
## Location of Jupyter Notebook:
The corresponding Jupyter Notebook that was used to analyze the dataset and create the following charts is located in Github at the following location:
 
https://github.com/andrespineda/Comparing Classifiers

 
## Background
 
As part of the UC Berkeley Professional Certificate in Machine Learning
and Artificial Intelligence (UC Berkeley, 2022), this assignment is the
third practical application designed to test our new skills. We are to use the Cross Industry Standard Process for Data Mining (CRISP-DM) method
(SchrÃ¶er, et al, 2021) of data analysis, see Figure 1 below, on a
dataset of car prices.
 
<img src="./media/image1.png" style="width:3.54526in;height:3.55in"
alt="A diagram of the CRISP-DM Process Flow" />
 
Figure 1: The Cross Industry Standard Process for Data Mining (CRISP-DM)
 
**CRISP-DM**
 
The CRISP-DM (Cross-Industry Standard Process for Data Mining) approach
to data analysis involves six major steps as outlined below:
 
- Understanding the Business: This initial step involves conducting an
  in-depth analysis of the business objectives and needs. It includes
  assessing the current situation, defining goals based on insights, and
  setting up a plan to proceed.
 
- Understanding the Data: In this phase, data is collected from various
  sources, its format and type are determined, and the data is profiled.
  Tasks include exploring the data, describing it, and ensuring its
  quality, accuracy, and validity.
 
- Data Preparation: Careful selection, cleansing, construction, and
  formatting of the data are carried out in this step. The data is
  organized for modeling, and information exploration is conducted to
  identify patterns aligned with business insights.
 
- Modeling: The modeling phase involves selecting modeling techniques,
  generating test scenarios for validation, building various models, and
  assessing them to ensure alignment with business objectives
 
- Evaluation: During this phase, the results of the models are evaluated
  against business intentions. Multiple models are assessed to determine
  which one best meets the project's goals.
 
- Deployment/Communication: The final step involves presenting the
  gathered information in a usable manner to stakeholders according to
  their expectations and business requirements. This phase may vary in
  complexity based on numerous factors.
 
## Scope of this Assignment
 
This practical application covers the following sections of the CRISP-DM methodology: Understanding the Business, Understanding the Data, Data Preparation, Modeling, and Evaluating.
 
## Understanding the Business
 
Understanding which vehicle features increase the price of a vehicle is crucial for a used vehicle dealer for several reasons:
 
1. **Pricing Strategy**: Knowledge of value-adding features allows dealers to price their vehicles competitively and accurately. They can ensure a fair profit margin while still offering attractive prices to customers.
 
2. **Inventory Selection**: Dealers can make informed decisions about which cars to acquire for their inventory. By focusing on vehicles with features that are in high demand, they can turn over their inventory more quickly and efficiently.
 
3. **Sales Focus**: When interacting with customers, salespeople can highlight the features that justify a car's price, helping to validate the value proposition to potential buyers.
 
4. **Market Trends**: Awareness of which features are currently increasing a car's value helps dealers stay ahead of market trends and adapt their sales strategies accordingly.
 
5. **Trade-in Evaluations**: When appraising vehicles for trade-in, dealers must understand the impact of various features on a car's value to offer fair trade-in prices that protect their bottom line.
 
6. **Targeted Marketing**: Dealers can tailor their marketing efforts to emphasize the most valuable features of their vehicles, attracting buyers who are willing to pay more for those specific attributes.
 
7. **Customer Satisfaction**: By understanding and meeting customer demand for certain features, dealers can improve customer satisfaction and potentially generate repeat business and referrals.
 
In summary, knowing which features increase a car's price helps used vehicle dealers manage their business more effectively, from inventory acquisition and pricing to sales strategies and customer service (Muller, 2017).
 
 
**Business Objectives**
 
The business objective is to assess a database of used cars that contain their selling price and a list of features of the car. By analyzing this data, we can evaluate the price of the vehicle in comparison with the listed features of the car. Using this information, we are to build a model that can be used to evaluate other cars that we may want to sell in the used vehicle lots.
 
## Data Understanding
 
Various tools and resources are used for conducting the Data
Understanding step.
 
**Dataset**
 
The dataset used for this assignment was provided as part of the
assignment in a Comma Separated Values (CSV) format.
 
The dataset is organized in a tabular fashion with each row representing
a single vehicle and its features along with the price of the car.
 
As described in the assignment, the attributes of this dataset include:
 
Car attributes
 
* 'id' - a unique number assigned to this car,
* 'region' - the region within a state where the vehicle is located.
* 'price' - the current selling price of the car.
* 'year' - the year the vehicle was manufactured.
* 'manufacturer' - the vehicle manufacturer.
* 'model' - the model of the car.
* 'condition' - the condition of the car.
* 'cylinders' - the number of cylinders in the engine of this car.
* 'fuel' - the type of fuel required to operate this car.
* 'odometer' - the current mileage reading on the car's odometer.
* 'title_status' - indicates if there is a clear title to this car.
* 'transmission' - the type of transmission in the car.
* 'VIN' - the vehicle id number assigned to this car.
* 'drive' - whether this is a rear drive or 4 wheel drive vehicle.
* 'size' - the size of the car.
* 'type' - the type of car.
* 'paint_color' - the color of the car.
* 'state' - the U.S. state in which this vehicle is located.
 
 
## EDA
 
### Average Price Chart
The chart below depicts the range of prices for the cars in the dataset. The distribution of prices has a peak to the left of the mean price of $15,955.
 
The distribution appears to be right-skewed, with a long tail extending towards higher prices. This suggests that while most of the cars are clustered around the mean price, there is a significant number of cars with higher prices, which could represent luxury or high-performance vehicles.
 
The plot does not show a clear indication of a bimodal distribution, which would be characterized by two distinct peaks. Instead, there is one clear peak and a gradual decline in density as the price increases. The presence of a long tail towards the higher prices suggests that there are a smaller cluster of higher-priced cars.
 
<img src="./media/average price.png" style="width:3.54526in;height:3.55in"
alt="Average Price Chart" />
 
### Violin Plot
A Violin Plot is a visual tool that displays the price distribution of each feature in the dataset. The shape of the violin is determined by the variation of prices that are in the dataset for that feature as it relates to the price of the car.
 
<img src="./media/Violin Plots of All Features.png" style="width:3.54526in;height:3.55in"
alt="Violin Chart" />
 
From the violin plot, we can infer the following conclusions about the distribution of car prices with respect to different features:
##### Manufacturer:
  There is variation in price distribution among different manufacturers. Some manufacturers have a wider range of prices, while others have a more concentrated distribution, indicating that certain manufacturers may cater to different market segments.
##### Model:
  The price distribution varies significantly across different car models. Some models have a wide distribution, suggesting a range of options at different price points, while others are more concentrated.
##### Condition:
Cars in excellent condition tend to have a higher median price and a wider distribution, indicating a range of prices within the 'excellent' category. Cars in lower condition categories have a more concentrated distribution, with lower median prices.
##### Transmission:
  Automatic transmission cars have a wider price distribution compared to manual transmission cars, which could suggest a higher demand or a greater variety of features and models available with automatic transmissions.
##### Drive:
  The distribution of prices for cars with different drive types (fwd, rwd) shows variation, with some drive types having a wider range of prices.
##### Size:
  Compact cars have a more concentrated price distribution, while full-size cars have a wider distribution, indicating a greater variety of price points within the full-size category.
##### Cylinders:
  The number of cylinders is associated with different price distributions. Cars with more cylinders tend to have a higher median price and a wider distribution, which may reflect higher performance or luxury models.
##### Type:
  Different car types (sedan, SUV, truck, etc.) have distinct price distributions, with some types having a wider range of prices, which could be due to differences in utility, features, and market demand.
##### Color:
  The distribution of prices also varies by color, with some colors having a wider distribution than others, which might reflect consumer preferences or the availability of certain colors in higher-end models.
##### Area:
  The area feature shows different price distributions, which could indicate regional variations in car prices due to factors like demand, economic conditions, or availability.
##### Odometer Range:
  Cars with different odometer readings show varying price distributions, with newer cars (lower odometer readings) generally having higher prices.
##### Summary
These insights from the violin plot can be valuable for understanding the factors that influence car prices.
Further analysis will determine which features have the most impact on car prices.
 
### Box Plot
### Box Plot Analysis
From the box plot, we can infer the following conclusions about the distribution of car prices with respect to different features
 
<img src="./media/Price_Distribution_by_Feature.png" style="width:3.54526in;height:3.55in"
alt="Price Distribution Chart" />
#### Manufacturer:
  There is variation in price distribution among different manufacturers. Some manufacturers have a wider range of prices, while others have a more concentrated distribution, indicating that certain manufacturers may cater to different market segments.
#### Model:
  The price distribution varies significantly across different car models. Some models have a wide distribution, suggesting a range of options at different price points, while others are more concentrated.
#### Condition:
  Cars in excellent condition tend to have a higher median price and a wider distribution, indicating a range of prices within the 'excellent' category. Cars in lower condition categories have a more concentrated distribution, with lower median prices.
#### Transmission:
  Automatic transmission cars have a wider price distribution compared to manual transmission cars, which could suggest a higher demand or a greater variety of features and models available with automatic transmissions.
#### Drive:
  The distribution of prices for cars with different drive types (fwd, rwd) shows variation, with some drive types having a wider range of prices.
#### Size:
  Compact cars have a more concentrated price distribution, while full-size cars have a wider distribution, indicating a greater variety of price points within the full-size category.
#### Cylinders:
  The number of cylinders is associated with different price distributions. Cars with more cylinders tend to have a higher median price and a wider distribution, which may reflect higher performance or luxury models.
#### Type:
  Different car types (sedan, SUV, truck, etc.) have distinct price distributions, with some types having a wider range of prices, which could be due to differences in utility, features, and market demand.
#### Color:
  The distribution of prices also varies by color, with some colors having a wider distribution than others, which might reflect consumer preferences or the availability of certain colors in higher-end models.
#### Area:
  The area feature shows different price distributions, which could indicate regional variations in car prices due to factors like demand, economic conditions, or availability.
#### Odometer Range:
  Cars with different odometer readings show varying price distributions, with newer cars (lower odometer readings) generally having higher prices.
 
These insights from the box plot can be valuable for understanding the factors that influence car prices and can inform the feature selection and engineering process in machine learning model development. By identifying the features with the most significant impact on price, we can prioritize these for inclusion in the model to improve its predictive accuracy. Additionally, understanding the distribution of prices can help in detecting outliers and in transforming features to better capture the underlying patterns in the data.
 
## Correlation Heatmap
 
<img src="./media/Correlation Heatmap.png" style="width:3.54526in;height:3.55in"
alt="Price Distribution Chart" />
The heatmap displays correlation coefficients ranging from -1 to 1. Values close to 1 or -1 indicate strong positive or negative correlations, respectively, while values close to 0 indicate a weak or no linear correlation. Price is the target variable and is the diagonal values = 1. There are several that show near perfect correlation, indicating that they are likely representing the same or very similar models and could be redundant in the dataset, for example "model_grand and model_l-100."
Other than those, the highest are:
* model_accord: This feature has a correlation of 0.23 with the target variable 'price'.
* model_camry: This feature has a correlation of 0.23 with 'price'.
* odometer_range: This feature has a correlation of 0.22 with 'price'.
* model_civic: This feature has a correlation of 0.22 with 'price'.
* model_altima: This feature has a correlation of 0.22 with 'price'.
 
 
## Modeling
After reviewing the data, several models were created to determine the impact of the various features in the dataset on the price. Several regression models were created and tested.
The following types of models were tested:
* Linear Regression
* Ridge
* LASSO
 
* Degree 2
* Degree 3
 
Also, Cross Validation techniques were used to verify the models and to determine which model would be best at predicting the price of a car in a new dataset:
 
* K-Fold Cross VValidation
* GridSearchCV
 
After the modeling, we evaluatede the R2 and MSE to determine the best model that can be used to predict car prices.
 
<img src="./media/Model_Perforamance_Comparison.png" style="width:3.54526in;height:3.55in"
alt="Model Scores" />
 
  ### Evaluation of Model Scores
  **Model Performance Evaluation:**
- **Logistic Regression:** Achieved a test accuracy of 89.39% with the best parameters C=1 and solver='liblinear'. This indicates that the model can effectively predict customer subscription to term deposits based on the provided features.
- **Decision Tree:** Obtained a test accuracy of 89.39% with the best parameters max_depth=50, min_samples_split=2, and min_samples_leaf=1. This suggests that the model can capture complex relationships between features and the target variable.
- **KNN:** Delivered a test accuracy of 89.39% with the best parameters n_neighbors=7, weights='uniform', and metric='euclidean'. This implies that using a small number of neighbors and uniform weighting can effectively identify similar customers for subscription prediction.
- **SVM:** Achieved a test accuracy of 89.39% with the best parameters C=100, kernel='rbf', and gamma='scale'. This indicates that the model can effectively separate data points into classes using a non-linear decision boundary.
**Insights:**
- All four models demonstrated comparable performance in terms of test accuracy. This suggests that different types of models can be suitable for this classification problem.
- The relatively high accuracy scores indicate that the encoded features are informative and contribute to the model's ability to predict customer subscription.
- Further analysis and model tuning could potentially improve the accuracy and performance of the models.
The results highlight the importance of comparing different models and tuning their hyperparameters to achieve the best predictive performance on the given dataset.

**Precision, Recall, and F1 Scores:**

The model with the highest precision score is KNN, with a score of 0.95. This means that out of all the customers it predicted as likely to subscribe to a term deposit, 95% actually did.
The model with the highest recall score is Logistic Regression, with a score of 0.92. This means that out of all the customers who actually subscribed to a term deposit, 92% were correctly identified by the model.
The model with the highest F1 score is also KNN, with a score of 0.91. This means that the model has a good balance between precision and recall, correctly identifying a high proportion of customers who subscribed to a term deposit while minimizing false positives.
Overall, all four models performed well in terms of precision, recall, and F1 score. However, KNN and Logistic Regression emerged as the top performers, with KNN having a slight edge in terms of precision and F1 score, while Logistic Regression had a higher recall score.
 
 
## Next Steps
 
The next steps in this process will be the Evaluation, and
Deployment/Communication steps in the CRISP-DM methodology. These steps will require skills that we currently have not studied, but we are looking forward to learning these techniques.
 
 
## References
 
Muller, D. (2017, November 14). How equipment choices affect a carâ€™s resale value. Weighing Your Options: How Equipment Choices Affect a Carâ€™s Resale Value. https://www.caranddriver.com/news/a15338786/weighing-your-options-how-equipment-choices-affect-a-cars-resale-value/
 
 
SchrÃ¶er, Christoph & Kruse, Felix & Marx GÃ³mez, Jorge. (2021). A
Systematic Literature Review on Applying CRISP-DM Process Model.
Procedia Computer Science. 181. 526-534. 10.1016/j.procs.2021.01.199.
 
UC Berkeley. (August 30, 2022). â€œUC Berkeley Professional Certificate in
Machine Learning and Artificial Intelligenceâ€. UC Berkeley.
https://em-executive.berkeley.edu/professional-certificate-machine-learning-artificial-intelli
