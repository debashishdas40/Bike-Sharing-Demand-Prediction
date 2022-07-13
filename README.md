
# Bike-Sharing-Demand-Prediction
![Cycling Youtube Thumbnail](https://user-images.githubusercontent.com/30859632/178668188-e849665d-a517-4312-9f8c-b08f9ba29413.png)
Problem Description
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.


# Features description
Breakdown of Our Features:

Date : The date of the day, during 365 days from 01/12/2017 to 30/11/2018, formating in DD/MM/YYYY, type : str, we need to convert into datetime format.

Rented Bike Count : Number of rented bikes per hour which our dependent variable and we need to predict that, type : int

Hour: The hour of the day, starting from 0-23 it's in a digital time format, type : int, we need to convert it into category data type.

Temperature(°C): Temperature in Celsius, type : Float

Humidity(%): Humidity in the air in %, type : int

Wind speed (m/s) : Speed of the wind in m/s, type : Float

Visibility (10m): Visibility in m, type : int

Dew point temperature(°C): Temperature at the beggining of the day, type : Float

Solar Radiation (MJ/m2): Sun contribution, type : Float

Rainfall(mm): Amount of raining in mm, type : Float

Snowfall (cm): Amount of snowing in cm, type : Float

Seasons: *Season of the year, type : str, there are only 4 season's in data *.

Holiday: If the day is holiday period or not, type: str

Functioning Day: If the day is a Functioning Day or not, type : str

# Preprocessing the dataset
Handle missing values

Duplicate values
Changing data type


# Exploratory Data Analysis Of The Data Set
# Why do we perform EDA?

An EDA is a thorough examination meant to uncover the underlying structure of a data set and is important for a company because it exposes trends, patterns, and relationships that are not readily apparent.
Univariate Analysis
Why do you do univariate analysis?

The key objective of Univariate analysis is to simply describe the data to find patterns within the data.
Analysis of Dependent Variable:
What is a dependent variable in data analysis?

we analyse our dependent variable,A dependent variable is a variable whose value will change depending on the value of another variable.
Analysation of categorical variables
Our dependent variable is "Rented Bike Count" so we need to analysis this column with the other columns by using some visualisation plot.first we analyze the category data tyep then we proceed with the numerical data type

# Hours image


https://github.com/debashishdas40/Bike-Sharing-Demand-Prediction/issues/4#issue-1303046757


From the above point plot and bar plot we can say that in the week days which represent in blue colur show that the demand of the bike higher because of the office.
Peak Time are 7 am to 9 am and 5 pm to 7 pm*
The orange colur represent the weekend days, and it show that the demand of rented bikes are very low specially in the morning hour but when the evening start from 4 pm to 8 pm the demand slightly increases.*

# Season Wise by dayHours


https://github.com/debashishdas40/Bike-Sharing-Demand-Prediction/issues/5#issue-1303047287

In the above bar plot and point plot which shows the use of rented bike in in four different seasons, and it clearly shows that,
In summer season the use of rented bike is high and peak time is 7am-9am and 7pm-5pm.
In winter season the use of rented bike is very low because of snowfall.




# Booking count analysys Holiday and Non holidays

https://github.com/debashishdas40/Bike-Sharing-Demand-Prediction/issues/6#issue-1303048002


In the above bar plot and point plot which shows the use of rented bike in a holiday, and it clearly shows that,
plot shows that in holiday people uses the rented bike from 2pm-8pm


# Heatmap
we check correletion betweeen variables using Correlation heatmap, it is graphical representation of correlation matrix representing correlation between different variables
https://github.com/debashishdas40/Bike-Sharing-Demand-Prediction/issues/3#issue-1303044276


We can observe on the heatmap that on the target variable line the most positively correlated variables to the rent are :

the temperature
the dew point temperature
the solar radiation
And most negatively correlated variables are:

Humidity
Rainfall

Feature Encoding Techniques
Model Training
Linear regression
1	Lasso regression	
2	Ridge regression	
3	Elastic net regression
4 Dicision tree regression	
5	Random forest regression	
6	Gradient boosting regression	
7	Gradient Boosting gridsearchcv	






Hyperparameter tuning
Before proceding to try next models, let us try to tune some hyperparameters and see if the performance of our model improves.

Hyperparameter tuning is the process of choosing a set of optimal hyperparameters for a learning algorithm. A hyperparameter is a model argument whose value is set before the learning process begins. The key to machine learning algorithms is hyperparameter tuning.

Using GridSearchCV

GridSearchCV helps to loop through predefined hyperparameters and fit the model on the training set. So, in the end, we can select the best parameters from the listed hyperparameters.

![image](https://user-images.githubusercontent.com/30859632/178679404-fa34c847-0656-4f03-961b-993993877b98.png)


https://github.com/debashishdas40/Bike-Sharing-Demand-Prediction/issues/7#issue-1303051468

# CONCLUSION

During the time of our analysis, we initially did EDA on all the features of our datset. We first analysed our dependent variable, 'Rented Bike Count' and also transformed it. Next we analysed categorical variable and dropped the variable who had majority of one class, we also analysed numerical variable, found out the correlation, distribution and their relationship with the dependent variable. We also removed some numerical features who had mostly 0 values and hot encoded the categorical variables.

Next we implemented 7 machine learning algorithms Linear Regression,lasso,ridge,elasticnet,decission tree, Random Forest and XGBoost. We did hyperparameter tuning to improve our model performance. The results of our evaluation are:
