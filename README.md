# what drives the price of a Car ?

# Introduction

In this application, we will delve into a dataset of pre-owned cars sourced from Kaggle. The objective of this endeavor is to discern the factors influencing the pricing of cars, ultimately providing recommendations to our client, a used-car dealership, regarding consumer preferences in pre-owned vehicles.

The project will entail the construction of several machine learning regression models, with subsequent assessment of their performance. Employing regression algorithms including Lasso Regression, Ridge Regression, Decision Tree Regressor, and Gradient Boosted Regressor, we will scrutinize the outcomes to identify the most effective model. Additionally, we will explore and elaborate upon the significance of various features impacting car prices through feature importance analysis.

# Dataset

The dataset utilized in this project is derived from Kaggle, which can be accessed [here.](https://mo-pcco.s3.us-east-1.amazonaws.com/BH-PCMLAI/module_11/practical_application_II_starter.zip) The dataset is extensive, comprising over 24 million credit card transactions. 

**Exploratory data analysis:**

The dataset consists of 18 features alongside a target continuous feature indicating the price of the used car. There were lot of outliers observed in te initial analysis. Null values were observed in all features except 'id', 'region', 'price' and 'state'. 

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

**Data Visualization:**

![Cars by Title Status](/images/carsbyTitle.png)

![Fuel Type vs Cylinders](/images/fuelTypeCylinders.png)

![Types of Manufactures](/images/manufacturers.png)

# Models Evaluation and Comparison



**Lasso Regression:**



**Ridge Regression:**



**Decision Tree Regressor:**



**Gradient Boost Regressor:**



| MODEL | MSE  Train  |  MSE  Test |
|:---:|:---:|:---:|
| Lasso Regression |  |  |
| Ridge Regression |  |  |
| Decision Tree Regressor  | |  |
| Gradient Boost Regressor |  |  |


# Summary of Findings



# Notebook

[Used Car Pricing](/.ipynb)
