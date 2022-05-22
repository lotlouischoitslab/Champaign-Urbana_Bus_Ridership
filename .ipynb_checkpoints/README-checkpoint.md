# Champaign-Urbana Bus Ridership Analysis & Prediction
## Contributors:
- ### Louis Sungwoo Cho 조성우



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


As an undergraduate student who is majoring in civil engineering specializing in transportation engineering and minoring in computer science at UIUC, I would frequently use the CUMTD bus to travel around campus. Either to go to I-Hotel so I could attend civil engineering conferences or go to the South Quad which is very far from the Engineering area (CIF, Grainger Library, Newmark CEE Laboratory, Thomas Siebel Center for CS, ECEB, Sidney Lu MEB, the list goes on). I would also ride the bus to go to downtown Champaign and Urbana to get some delicious food too! I always wondered what the daily ridership would be for these buses and whether the ridership would increase or not.


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


# Machine Learning and Dataset Training


The datasets given were trained to determine how accurate the models are to predict the total passenger ridership for each month. The Decision Tree, Random Forest algorithms were used to train the datasets. Using the Decision Tree Regressor, the mean absolute error (MAE) fluctuated variously meaning that this model is not the most optimal choice to train the given dataset. To minimize the MAE, the Random Forest Algorithm was used to determine the MAE with a lower fluctuation. The Random Forest Algorithm gave an approximate MAE value of 350535. 


$$ MAE\ =\ \frac{1}{n} \sum_{i=1}^{n} \ |y_i\ -\ \hat{y}_i| \ $$


The formula above shows the Mean Absolute Error (MAE) used to train the dataset.


# Time Series Forecasting

```python
s
```
