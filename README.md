# Introduction
The aim of this report is to present the development and analysis of a taxi price prediction model. The model seeks to predict the trip price of a taxi ride based on several key factors including distance, traffic conditions, weather, base fare, and trip duration in minutes. This report will outline the importance of each independent variable and discuss how they influence the predicted taxi fare.

## Objective
The primary objective of the model is to predict the trip price based on input features that are typically recorded during a taxi trip. By incorporating multiple factors, the model provides a comprehensive approach to estimating the cost of a taxi ride.

## Independent Variables:
- Distance: The total distance of the trip, usually measured in miles or kilometers.
-	Traffic Conditions: This variable reflects the impact of traffic congestion, which can either increase or decrease travel time and, consequently, trip price.
-	Weather: Weather conditions can influence traffic patterns, driver behavior, and the overall comfort and safety of the trip.
-	Base Fare: The initial fare for the ride, which is set by the taxi service as a fixed charge before additional charges are applied.
-	Trip Duration: The total time taken for the trip, typically measured in minutes.

## Dependent Variables
-	Trip Price: The total cost of the taxi ride, which is influenced by the above variables.


## Data Collection
The model relies on data collected from actual taxi trips. The data includes the following features:
-	Distance: Measured in kilometers or miles.
-	Traffic Conditions: Categorical data (e.g., light, moderate, heavy) or numerical data (e.g., average speed).
-	Weather: Categorical data indicating conditions such as clear, rainy, snowy, etc.
-	Base Fare: The constant initial charge set by the taxi service.
-	Trip Duration: The length of the trip measured in minutes.
-	Trip Price: The total fare for the trip, including any additional charges based on the above variables.

## Feature Engineering
To enhance the model's ability to predict trip prices accurately, the following transformations and considerations were applied to the independent variables:

Distance:
- Distance is typically one of the primary factors affecting trip price. As the distance increases, the price of the trip also rises, assuming other factors remain constant.
Traffic Conditions:
- Traffic data, which can be either categorical (e.g., light, moderate, heavy) or numerical (e.g., average speed), has a significant impact on the time taken to complete a trip. Higher congestion leads to longer trip durations and may increase the fare.
-	Traffic congestion may be modeled as a time-based or speed-based variable.
Weather:
-	Weather conditions can affect traffic patterns, as rain or snow often leads to slower speeds and increased trip duration. Weather can be encoded as categorical data (e.g., sunny, rainy, snowy) or numeric data (e.g., temperature, wind speed) depending on data availability.
-	Extreme weather conditions such as storms may also lead to higher fares due to potential detours or delays.
Base Fare:
-	The base fare is generally a fixed cost that is set by the taxi company. It does not vary with the distance or time, but it serves as an essential component of the total trip price.
-	It is treated as a constant input in the model.
Trip Duration:
-	Trip duration is a direct indicator of the time spent in the taxi. The longer the trip, the higher the fare, assuming that the base fare and distance are relatively fixed.
-	Duration is usually measured in minutes and directly correlates with the overall price of the trip.

## Model Development
A predictive model was developed using machine learning techniques such as Linear Regression, Decision Trees, and Random Forest to analyze the relationship between the independent variables and the target variable, trip price.

Model Selection:
-	Linear Regression: A simple and interpretable model to predict continuous variables. It assumes a linear relationship between the independent variables and the trip price.
-	Decision Trees: A more flexible model that can capture non-linear relationships in the data, such as when certain traffic conditions lead to a sharp increase in trip duration.
-	Random Forest: An ensemble learning method that combines multiple decision trees to improve accuracy and reduce overfitting.

Model Evaluation:
-	Mean Absolute Error (MAE): This metric calculates the average of the absolute errors between predicted and actual values. It provides a clear understanding of the magnitude of error in terms of the price.
-	Root Mean Square Error (RMSE): A widely used metric that penalizes large errors more heavily than smaller ones, helping to identify models that perform well in general.
-	R-Squared (R²): This indicates the proportion of the variance in the dependent variable (trip price) that is predictable from the independent variables.

## Results
The model demonstrated the following key findings:
-	Distance had the most significant positive correlation of 0.86 with trip price, as expected. An increase in distance led to a higher predicted price.
-	Traffic Conditions showed a low positive effect on trip price. Higher traffic congestion caused a slight increase in trip duration, which in turn increased the fare.
-	Weather was found to have a very low  positve relationship with trip price.
-	Base Fare had a minimal effect on the prediction, as it was constant across trips but essential for setting the baseline fare.
-	Trip Duration had a low significant impact on price prediction.


## Conclusion
The taxi price prediction model effectively estimates the cost of a taxi ride by taking into account distance, traffic conditions, weather, base fare, and trip duration in minutes. Key findings highlight that trip duration and traffic conditions are among the most significant predictors of the trip price, with weather and distance also contributing to the model's accuracy.
Future work could focus on further tuning the model by exploring additional features such as driver behavior, time of day, or ride-sharing options. Moreover, using real-time data such as GPS tracking and live weather updates could further enhance the accuracy and reliability of the model.

## Recommendations:
-	Taxi companies should consider traffic conditions and the distance covered when providing fare estimates to customers.
-	The model could be integrated into ride-hailing applications to offer users real-time price predictions based on current conditions.



# How to use the model
This model is used to predict taxi trip price based on five various independent variables such as distance , traffic conditions, weather, base fares, and duration in minutes. It provides realistic synthetic predictions for regression tasks, offering a unique opportunity to explore pricing trends in the taxi industry.

# The Model
Y = B0 + B1X1 + B2X2 + B3X3 + B4X4 + B5X5 
B0 = is the intercept(-13.65)
B1 = distance
B2 = traffic conditions
B3 = weather
B4 = base fares
B5 = duration in minutes

Traffic conditions is been converted from categorical variable to quantitative variables were:
- Low = 1
- Medium = 2
- High = 3

Weather also:
- Clear = 1
- rain = 2
- snow = 3

It was predicted that it cost $41.65 to go on a distance of 19.35km at low traffic condition on a clear road with a 3.56 base fare at 60 minutes.
  

