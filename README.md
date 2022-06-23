# Champaign-Urbana Bus Ridership Analysis & Prediction
## Contributors:
- ### Louis Sungwoo Cho UIUC CEE/CS 2024



# Project Description


![Alt text](https://yourewelcomecu.com/wp-content/uploads/2015/09/Church-Neil-web.jpg)


#### A 5W GREEN hopper bus approaches a bus stop shown above. 
- Image source: https://yourewelcomecu.com/cumtd-bus-photos/


This project is about analyzing and predicting the ridership of the buses in the Champaign-Urbana area operated by the Champaign-Urbana Mass Transit District also known as CUMTD. Datasets were acquired from the official Champaign County Regional Data Portal which could be found here:
- https://data.ccrpc.org/da_DK/dataset/transit-ridership

Datasets from the years 1997 to 2022 and months of July, October, December and February were used to analyze and predict the passenger volume for the bus.


![Alt text](https://mtd.org/media/1096/weekday-daytime-no-insets.png?anchor=center&mode=crop&width=1200&height=720&rnd=132734497340000000)


The image above shows the CUMTD bus network that connects Campustown, Champaign and Urbana. Image downloaded from:
- https://mtd.org/maps-and-schedules/maps/

As shown in the image above, the CUMTD bus network is very dense connecting almost all the popular places visited by many passengers.


# Motivation

The Champaign-Urbana Mass Transit District also known as (CUMTD) serves as a great public transportation system throughout the entire University of Illinois at Urbana-Champaign area and a crucial type of mobility for university students to travel around on campus. From Grainger Library, Campus Instructional Facility (CIF), Newmark Civil Engineering Laboratory, Thomas Siebel Center for Computer Science, Electrical & Computer Engineering Building, Sidney Lu Mechanical Engineering Building to Business Instructional Facility, Altgeld Hall, Main Library, Foellinger Auditorium and many more wonderful places, you could almost travel anywhere by using the CUMTD buses. People even use the buses to go to downtown Champaign or to downtown Urbana to get some delicious food or to even go shopping, watch movies and even to enjoy some karaoke. As an Undergraduate Computational Transportation Scientist at UIUC, I decided to perform a traffic capacity analysis on the passenger ridership volume of the CUMTD buses and to perform time series forecasting to estimate the predicted passenger volume in the near future.

# Monthly Ridership Trend Analysis


This section analyzes the passenger riderhip trend in four different months: October, July, February and December in addition to the total number of passengers with respect to years from 1997 to 2021. A scatter plot including all the monthls and the total bus ridership passenger analyzed from the years 1997 to 2021 were also plotted.


![title](images/describe.jpg)


#### Figure 1. shows the mean, standard deviation, minimum value, 25 percentile, 50th percentile, 75th percentile and the maximum values respectively for each month analyzed and the total passenger ridership 


![title](images/anual.png)


#### Figure 2. above shows the scatter plot of all the data including both months and total ridership


![title](images/scatter.png)


#### Figure 3. above shows the ridership of the CUMTD bus broken down into months


Datasets were then further broken down into months and total ridership to determine the line of best fit for all the plotted data points. The following figure shows a polynomial regression of degree 3 line curve plotted with respect to the analyzed data.


![title](images/oct.png)


#### Figure 4. above shows the line of best fit for the October passenger ridership with respect to the years from 1997 to 2021.


![title](images/july.png)


#### Figure 5. above shows the line of best fit for the July passenger ridership with respect to the years from 1997 to 2021.


![title](images/feb.png)


#### Figure 6. above shows the line of best fit for the February passenger ridership with respect to the years from 1997 to 2021.


![title](images/dec.png)


#### Figure 7. above shows the line of best fit for the December passenger ridership with respect to the years from 1997 to 2021.


![title](images/tot.png)


#### Figure 8. above shows the line of best fit for the total passenger ridership with respect to the years from 1997 to 2021.


Although all the figures above called the function to perform data analysis and determine the line of best fit using the linear regression method, the data scattered shows that the trend line approximately matches the plots using the degree of 3. Thus, polynomial regression is more suitable for the analyzed dataset. According to the monthly bus ridership plots with respect to time in years, there is an increasing trend. However around the year 2020, there has been a significant drop in monthly ridership and the total ridership with respect to years due to the COVID-19 pandemic.

# Data Cleaning 

![title](images/data_to_be_cleaned.png)

#### Figure 9. above shows the data that needs to be cleaned

The given dataset by the Champaign County Regional Data Portal neede some cleaning to be fitted appropriately for the time series forecasting model. The months had to be aligned sequentially with respect to each year from 1997 to 2021. New dataframe had to be created using the Pandas library. Months had to be adjusted in sequential order. To make the datasets consistent with the appropriate sequence, the dates have been adjusted by default to the starting day of that specific given month for each year. Pandas has another function which converts the independent variable to date and time format. The modified data frame was used for the time series analysis and forecasting for passenger volume. 

![title](images/cleaned_data.png)

### Figure 10. above shows the modified time data frame


![title](images/estimator.png)

### Figure 11. above shows the estimator for traffic trend analysis

An estimator curve was plotted to mathematically analyze the trend of the passenger volume of the CUMTD buses.The blue lines represent the recorded passenger ridership by the Champaign County Portal. The orange line shows the estimator line to approximate the passenger trend of the CUMTD buses. 



# Machine Learning and Dataset Training

Datasets were split into training datasets and testing datasets in the model. They were used to predict the total passenger ridership for each year with respect to the given months. 80% of the datasets were used for training and 20% of the datasets were used for testing the model. Once the predictions were made, three methods to test the performance of the model were used: Mean Absolute Error, Mean Squared Error, and Root Mean Squared.



$$ MAE\ =\ \frac{1}{n} \sum_{i=1}^{n} \ |y_i\ -\ \hat{y}_i| \ $$


The formula above shows the Mean Absolute Error (MAE) used to train the dataset.

$$ MSE\ =\ \frac{1}{n} \sum_{i=1}^{n} \ (y_i\ -\ \hat{y}_i|)^2 \ $$


# Time Series Forecasting

```python
s
```
