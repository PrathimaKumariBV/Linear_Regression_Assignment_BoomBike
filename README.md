# Multiple Linear Regression  Bike-Sharing Assignment

 A US bike-sharing provider BoomBikes aspires to understand the demand for shared bikes among the people after the ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits. 
 
 The company wants to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. 
 
 The company wants to know:
 * Which variables are significant in predicting the demand for shared bikes.
 * How well those variables describe the bike demands

## Table of Contents

* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information

### 1.Business Understanding

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

### Business Objectives:

We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

### 2.Data Description

Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors. 

### Feature Description

	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : wether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

### Objective of the Assignment

    * Build a Multiple Linear Regression model to predict the future demand for shared bikes.
    
    * Evaluate the model by statistical metrics
    
    * Find the independent variables which are significant in predicting the demand for shared bikes.
    

### 3. Data understanding
    - Understanding the data
    
### 4. Data Cleaning

    - Handling Missing values
    - Change the categorical variables numerical value to the associated string value for better understanding of data
    - 

### 5. EDA

#### 5.1 Summary statistics for numeric attribute
#### 5.2  Univariate Analysis
#### 5.2.2 Univariate Analysis for Categorical Variables 
##### barplot,count plot, pie plot
#### 5.2.1 Univariate Analysis for Continuous Variables
##### distribution plots,count plot 
#### 5.3 Visualization of Continuous Variables
##### Scatter plot, heatmap
#### 5.4 Visualization of Categorical Variables
##### box plot
#### 5.5 Conclusion

### 6. Data Preparation

#### 6.1. Create Dummy variables for all the categorical variables
#### 6.2. Divide the data into training and testing data
#### 6.3. Perform Scaling 
#### 6.4. Divide data into dependent and indipendent variables

### 7. Model Building

#### 7.1 Model 1: Included all the independent variables  
#### 7.2 Building Models using both 'RFE' method for automation of feature elimination and 'statsmodel' for the detailed statistics
#### 7.2.1 Model 2: (Build the model by considering top 15 features)
##### Model 2.1, Model 2.2, Model 2.3
#### 7.2.2 Model 3 : (Build the model by considering top 10 features)
#### 7.2.3 Model 4: (Build a model by removing the mnth_Nov from Model3)
#### 7.2.4 Model 5: (Build a model byconsidering top 7 features)

### 8. Residual Analysis

#### 8.1 Check R-square value
#### 8.2 Error terms Normality check
#### 8.3 Looking for patterns in the residuals

### 9. Prediction on the test dataset and Model Evaluation

#### 9.1 Scale the test dataset first
#### 9.2 Prediction with Model5 (Top 7 variables)
#### 9.3 Model 5 Evaluation
#### 9.4 Prediction with Model4 (Top 9 variables)
#### 9.5 Model 4 Evaluation


## Conclusions

**Business Insights:**

1. There is a high demand for the shared bikes in comming years. After corona lockdown, when the conditions become normal the 'Boom-Bikes' will get very good profit in shared bike business.

2. When there a misty weather and light-snow the most of the people are not coming out.So there is a less demand for shared bikes.

3. The demand for shared bike is reducing in spring season.The Boom bike company can give some **spring season offers** to increase the demand in this season. Expand the business in Spring season.

4. Whenever holiday is there the demand for shared bike is reducing. So the Company can give some **holiday offers** or promotions to increase the demand.

5.  The demand for shared bikes are more when the weather is clear,temp is high and there is least demand when there is snow fall.

6. In holiday the demand for shared bike is reduces.

7. December and January is the beginning of Spring and still winter effect will be there, snow fall will be there. Therefore the demand for shared bikes is less. From Feb onwards again it pickups.

8. July has pleasant weather, but still there is a small dip of demand for shared bikes, again in September it reaches maximum.

9. We can give some focus for the unknown reason for the small dip of demand in July.

10. Winter season starts from September to December, There fore after September the demand for shared bikes dips till January.

11. There would be less bookings during Light Snow or Rain, they could probably use this time to serive the bikes without having business impact.

When the situation comes back to normal, the company should come up with new offers during spring season, advertise a little when the weather is pleasant , on July month and holidays.

Significant variables to predict the demand for shared bikes:

    -holiday (Little Focus needed to improve the business in holidays )
    
    -temperature (When there is pleasant weather and temerature the demand for shared bikes will increases)
    
    -Season (More focus needed for Spring season)
    
    -months (Little focus needed to avoid the small dip in July month)
    
    -Year (After Covid-19 lockdowns and quarantines, when the situation comes normal definitely the demand for shared bikes will increases)
    
    -weather-situation (If the weather situation is mist and light snowfall, the company can focus on bike services)


## Technologies Used

- Jupyter Notbook (anaconda3)
- Python Language
- pandas library 1.4.1
- numpy library 1.22.2
- seaborn library 0.11.2
- matplotlib library 3.5.1
- sklearn library 0.23.2
- statsmodels library 0.12.0


## Acknowledgements
Thanks for Upgrad to give this assignment to learn. This is very inspiring assignement to learn many tools and techniques to analyze the data and draw the insights and build multilinear regression


## Contributors

Created by,
  -Prathima Kumari B V
  
Developed as part of the  Linear Regression module required for Advanced Certificate Program for ML and AI - IIIT,Bangalore.
