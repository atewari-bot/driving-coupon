# Assignment 5.1 - Will the Customer Accept the Coupon?

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those who did not.

[Link to Coupons Dataset](https://github.com/atewari-bot/driving-coupon/blob/main/data/coupons.csv)

[Link to Jupyter Notebook](https://github.com/atewari-bot/driving-coupon/blob/main/prompt.ipynb)

## Exploratory Data Analysis (EDA)

### Missing data handling

* Column"car": More than 99% of values are missing.
  ** Car column have more than 99% of values missing. The type of vehicle should not affect coupon acceptance. We could drop the car column or fill it with a value 'car'. I would drop the column as this column is agnostic of coupon acceptance with 99% missing values. 
* Columns "Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, Restaurant20To50": Missing values in the range of 1% to 2%.
  ** We replaced null values with mode of the column

## General data distributionn visulaization
![Image](/images/overall_coupons_acceptance_proportion.png)
<br>
<br>
![Image](/images/coupons_types_distribution.png)
<br>
<br>
![Image](/images/temperature_histogram.png)

## EDA Summary

### General Summary

* Overall 56.84% of coupons in various categories were accepted.
* Coffee House coupons were distributed the most and medium cost restuarent ($20 to $50) coupons were distributed the least.
* Drivers tend to accept more coupons on a sunny day.
  
### Bar coupons exploration summary

* Overall bar coupons acceptance rate is: 41 %
* Drivers with bar visits 3 or less tend to accept coupon 4.4 times more than the visitos who visit the bar more than 3 times a month.
* Drivers with age of 25 and more tend to accept bar coupons 2.47 times more than younger bar visitors.
* Acceptance rate for drivers with no passanger kids and no FFF occupation tend to accept 10% lesser coupons compared to other drivers.
* Drivers who were not widowed, have no kids passangers and often visit bar tends to accept coupon at the rate of 47.52 %.
* Drivers at age below 30 and who visit bar multiple times in a month tend to accept the coupon at the rate of 30.11 %.
* Drivers with income below 50k and who visit restaurent more than 4 times a month, tend to accept the coupon at the rate of 18.86 %.

### Hypothesis summary

Based on data exploration and observations, we can hypothesize following about the drivers who accepted the coupons:

* **Age Feature**: Younger drivers tend to accept more coupons. This indicates younger people tend to socialize more than older drivers, particulary driver younger than age of 30.
* **Bar Visits Frequency Feature**: Drivers who often visit bar, are highly likely to accept bar coupons. This indicate correlation between frequent bar visitors and their consideration to optimize their expenditure on bar visits.
* **Marital Status Feature**: Drivers who are not married are more likely to accept bar coupons. This shows social pattern where drivers with married partner are less inclined to visit bar.
* **Occupation Feature**: Drivers outside of farming, fishing and forestry are highly likey to accept bar coupons. This indicates people in other occupation have more lesiure time after the work.

## Independent Investigation - CoffeeHouse Coupon acceptance 

Coffee house coupons are the most number of coupons distributed to drivers. Will explore CoffeeHouse coupon to understand the customer behavior.

## General data distributionn visulaization
![Image](/images/ch_overall_acceptance.png)
<br>
<br>
![Image](/images/ch_drivers_comparision)
<br>
<br>
![Image](/images/ch_by_weather.png.png)
<br>
<br>
![Image](/images/ch_by_gender.png)
<br>
<br>
![Image](/images/ch_by_age.png)
<br>
<br>
![Image](/images/ch_by_education.png)
<br>
<br>
![Image](/images/ch_by_income.png)
<br>
<br>
![Image](/images/ch_by_marital_status.png)



