# what drives the price of a Car ?

# Introduction

In this application, we will delve into a dataset of pre-owned cars sourced from Kaggle. The objective of this endeavor is to discern the factors influencing the pricing of cars, ultimately providing recommendations to our client, a used-car dealership, regarding consumer preferences in pre-owned vehicles.

The project will entail the construction of several machine learning regression models, with subsequent assessment of their performance. Employing regression algorithms including Lasso Regression, Ridge Regression, Decision Tree Regressor, and Gradient Boosted Regressor, we will scrutinize the outcomes to identify the most effective model. Additionally, we will explore and elaborate upon the significance of various features impacting car prices through feature importance analysis.

# Dataset

The dataset utilized in this project is derived from Kaggle, which can be accessed [here.](https://mo-pcco.s3.us-east-1.amazonaws.com/BH-PCMLAI/module_11/practical_application_II_starter.zip) The dataset is extensive, comprising over 446 thousand records of used cars across the US. 

**Exploratory data analysis:**

The dataset consists of 18 features alongside a target feature indicating the price of the used car. There were lot of outliers observed in the initial analysis. Null values were observed in all features except 'id', 'region', 'price' and 'state'. 

| Feature        | Description                         |
| -------------- | ----------------------------------- |
| _Id_           | _Id of the Used-Car _               |
| _region_       | _Region where the car is present_   |
| _price_        | _Price of the used car_             |
| _year_         | _Year of Manufacture_               |
| _manufacturer_ | _Name of the Manufacturer_          |
| _model_        | _Model of the Manufacturer_         |
| _condition_    | _Known condition of the car_        |
| _cylinders_    | _Number of cylinders in the engine_ |
| _fuel_         | _Fuel Type of the car_              |
| _odometer_     | _Current Odometer reading_          |
| _title_status_ | _Title status of the car_           |
| _transmission_ | _Type of Transmission of the car_   |
| _VIN_          | _Vehicle Identification Number_     |
| _drive_        | _Drive Type of the car_             |
| _size_         | _Size of the Car_                   |
| _type_         | _Type of the car_                   |
| _paint_color_  | _Exterior paint color of the car_   |
| _state_        | _State where the car is registered_ |

Following data cleaning operations were performed

- Filling missing values in the 'year' column with the mode (most frequent) value from that column.
- Filling missing values in the 'condition' column with the mode value from that column.
- Filling missing values in the 'cylinders' column with the mode value from that column.
- Filling missing values in the 'fuel' column with the mode value from that column.
- Filling missing values in the 'title_status' column with the mode (most frequent) value from that column.
- Filling missing values in the 'transmission' column with the mode value from that column.
- Filling missing values in the 'drive' column with the mode value from that column.
- Filling missing values in the 'size' column with the mode value from that column.
- Filling missing values in the 'type' column with the mode value from that column.
- Filling missing values in the 'paint_color' column with the mode value from that column.
- Filling missing values in the 'odometer' column with the median value from that column.
- Filling missing values in the 'type' column again with the mode value from that column.
- Filling missing values in the 'manufacturer' column with the string 'unknown'.

**Data Visualization:**

![Cars by Type Cylinders](/images/carTypeCylinders.png)

The dataset is predominantly composed of numerous SUVs and Sedans in terms of vehicle types. When examining the number of cylinders, the dataset encompasses a range of options, including 3, 4, 5, 6, 8, 10, and 12 cylinders. Within the SUV and Sedan categories, 6-cylinder vehicles were the most commonly found. Conversely, trucks were observed to have the highest percentage of 8-cylinder vehicles.

![Fuel Type vs Cylinders](/images/fuelTypeCylinders.png)

The majority of vehicles were equipped with automatic transmission, with other classifications following. These other classifications might include unknown or a blend of automatic and manual transmission.

![Types of Manufactures](/images/manufacturers.png)

Among all manufacturers, Chevrolet, Toyota, Ford, and Honda had the highest number of cars. Several other manufacturers had a minimal number of cars.


# Models Evaluation and Comparison

In the regression analysis, Lasso, Ridge, Decision Tree Regressor, and Gradient Boost Regressor were evaluated. GridSearchCV was applied to all models to fine-tune the hyperparameters and cross validate. Due to computational constraints stemming from the dataset's complexity, exhaustive hyperparameter tuning was not feasible. Nevertheless, despite these limitations, the Decision Tree Regressor demonstrated superior performance, achieving notably low mean squared error (MSE) scores on both training and test datasets.

Below is a summary table presenting the results of the different ML regressor models:


**Regression**|**Train MSE**|**Test MSE**
:-----:|:-----:|:-----:
Lasso Regression  |0.39|0.38
Lasso Regression alpha : 0.02, max\_iter: 100)|0.38|0.38
Ridge Regression ('rdg\_\_alpha': 0.02)|0.39|0.38
Decision Tree Regressor (ccp\_alpha': 0.0)|0.014|0.29
GradientBoostingRegressor(learning\_rate: 0.025)|0.36|0.36

Finally for the decision tree regressor models, feature importance 

![Feature Importance](/images/featureImportance.png)

Odometer, Year, Transmission(Other), Car Size(Compact) and Paint Color(White) seems to be top features that seem to affect the price of the car.

# Summary of Findings

In conclusion, data quality significantly impacts the accuracy of predictions. Despite encountering outliers, we successfully cleaned the data, resulting in a more precise pricing model. To further enhance accuracy in the future, cleaner data would be beneficial. Additionally, our analysis revealed that odometer reading, car year, transmission type, compact car size, and white paint color are significant features influencing car prices. However, some outliers remain in the predictions. As a next step, efforts should focus on correcting the dataset at its source to address missing data more accurately. Subsequently, we can explore expanding the model with more advanced deep learning networks to evaluate their predictive accuracy.


# Notebook

[Used Car Pricing](/prompt_II.ipynb)
