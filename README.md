
<h1 align="center"> NYC Taxi Time Prediction </h1>
<h3 align="center"> AlmaBetter Verfied Project - <a href="https://www.almabetter.com/"> AlmaBetter </a> </h5>

<p align="center"> 
<img src="https://github.com/AnshRockstar/NYC-Taxi-Trip-Duration-Prediction/blob/main/Images/NYC%20Taxi.jpg" alt="NYC Taxi.jpg"  height="320px">
</p>

<p>I have clustered similar movies and TV Shows available on Netflix taking into account of attributes like Description, Cast, Director, Genre etc of a particular movie/show.</p>

<h2> :floppy_disk: Project Files Description</h2>

<p>This Project includes 1 colab notebook, 1 technical documentation as well as 1 presentation:</p>
<h4>Executable Files:</h4>
<ul>
  <li><b> NYC Taxi Trip Time Prediction - Capstone Project.ipynb</b> - Includes all functions required for regression operations.</li>
</ul>

<h4>Output:</h4>
<ul>
  <li><b>Google Colab</b> - All the outputs are visible in the provided colab notebook.
</ul>
<h4>Input Files:</h4>
<ul>
  <li><b>NYC Taxi.csv</b> - Input dataset having information about different shows/movies available on Netflix.</li>
</ul>
<h4>Data Source:</h4>
<li><b>https://learn.almabetter.com/courses/take/team-capstone-projects/texts/19499882-nyc-taxi-trip-time-prediction.</li>
<ul>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book:Introduction</h2>
More than 7 billion people exist on earth. With necessities of food, water and shelter there also a key requirement of commutating from one place to other. Rapid advancement in technology in the last two decades leads to adaption of a more efficient way of transportation via internet and app-based transport system. New York city is one of such advanced city with extensive use of transportation via subways, buses and taxi services. New York has more then 10,000 plus taxi and nearly 50% of population doesn’t have a personal vehicle. Due to this facts most people used taxi has a there primary mode of transport and it accounts for more than 100 millions taxi trips per year.

<h2> :book: Problem Statement</h2>
The main objective is to build a predictive model, which could help them in predicting the trip duration of taxi. This would in turn help them in matching the right cabs with the right customers quickly and efficiently.

<h2> :book: Data Summary</h2>
The dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform.
The data was originally published by the NYC Taxi and Limousine commission (TLC).
### The contents of NYC Taxi Time Prediction are:
  
*	id - a unique identifier for each trip.
*	vendor_id - a code indicating the provider associated with the trip record.
*	pickup_datetime - date and time when the meter was engaged.
*	dropoff_datetime - date and time when the meter was disengaged.
*	passenger_count - the number of passengers in the vehicle (driver entered value).
*	pickup_longitude - the longitude where the meter was engaged.
*	pickup_latitude - the latitude where the meter was engaged.
*	dropoff_longitude - the longitude where the meter was disengaged.
*	dropoff_latitude - the latitude where the meter was disengaged.
*	store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a         connection to the server - Y=store and forward; N=not a store and forward trip.
*	trip_duration - duration of the trip in seconds.



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# Exploring Solutions:
Having a deeper understanding of what problem we are trying to solve, what the users’ needs, and frustrations are, and what the goals are for achieving the best possible solution for both for the business as well as the user, I began by listing out the possible solutions that were arrived from the research.


# Steps involved:
The full code for this article can be found here. It is implemented in Python and different machine learning algorithms are used. Below is a brief description of the general approach that I employed:
* Data Loading and general checkups: 
We have loaded the data from the given csv files using a function from pandas library. Then we checked the general information about data
* Exploratory Data Analysis: 
We removed id variable as it doesn’t give much interpretation. We then calculated the distance based on haversine formula from pickup and drop-off latitude and longitude. Then we plotted the box plot for the variable and observed there are many outlier so we segregate this variable and see that most of the trip are within 10km, some trip are within 50km while a very few trip crosses 50km. so we eliminate trip with 0 and above 50km distance.
We then checked for categorical variable store_and_fwd_flag and passenger_count. We observed the store and fwd. flag contain majority of one category. So we drop this feature. Passenger count variable has entries from 0 to 9. Since there is no trips with 0 passenger either this a miss entry or the driver forgot to enter passenger count of that trip. Also in a taxi maximum six person are allowed to sit including minor. So we eliminate 0 and 7-9 records from our dataset.

* Linear Regression:
Linear Regression is a regression of dependent variable on independent variable. It is a linear model that assumes a linear relationship between dependent (y) and independent variables (x). 

* XGBoost:
XGBoost comes under boosting and is known as extra gradient boosting. GBM first calculates the model using X and Y then after the prediction is obtain. It will again calculates the model based on residual of previous model, here loss function will give more weightage to error of previous model. 

* LightGBM:
Light GBM is based on decision tree algorithm. But it splits the tree leaf wise rather then level wise like other boosting algorithm. So when growing on the same leaf in Light GBM, the leaf-wise algorithm can reduce more loss than the level-wise algorithm and hence results in much better accuracy which can rarely be achieved by any of the existing boosting algorithms.

# Conclusion
In this project we covered various aspects of the Machine learning development cycle. We observed that the data exploration and variable analysis is a very important aspect of the whole cycle and should be done for thorough understanding of the data. We also cleaned the data while exploring as there were some outliers which should be treated before feature engineering. Further we did feature engineering to filter and gather only the optimal features which are more significant and covered most of the variance in the dataset. Then finally we trained the models on the optimum featureset to get the results.


[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ansh-bhatnagar-093609117/)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshRockstar)
