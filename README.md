# Assignment 5.1 - Will the Customer Accept the Coupon?

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those who did not.

[Link to Coupons Dataset](https://github.com/atewari-bot/driving-coupon/blob/main/data/coupons.csv)

[Link to Jupyter Notebook](https://github.com/atewari-bot/driving-coupon/blob/main/prompt.ipynb)

## Exploratory Data Analysis (EDA)

### Missing data handling

* <b><i>car</i></b> column: More than 99% of values are missing.
  ** Car column have more than 99% of values missing. The type of vehicle should not affect coupon acceptance. We could drop the car column or fill it with a value 'car'. I would drop the column as this column is agnostic of coupon acceptance with 99% missing values. 
* <b><i>Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, Restaurant20To50</i></b> columns: Missing values in the range of 1% to 2%.
  ** We replaced null values with mode of the column

## Fix column name
* <b><i>passanger</i><b> column: Fixed typo of column name to correct spelling <i>passenger</i>

## General data distributionn visulaization
![Image](/images/coupons_acceptance_proportion.png)
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

**Overall Acceptance:** Overall 49.2% drivers accepted Coffee House coupon. This indicates there is a significant liklihood and opportunity to attract more customers by designing coupons based on deeper understanding of customer behavior and colloborating with businesses.
<br>
<br>
![Image](/images/ch_drivers_comparision.png)

**Different Segments Comparision:** In general, customers are inclined to accept more coffee house coupons on a sunny day.
<br>
<br>
![Image](/images/coffee_house_subplots.png)

**Segment-wise Acceptance Trend:**
* Sunny weather is most preferred day for accepting coffe house coupons
* Female drivers tend to accept more coupons than male drivers.
* Age range 21-26 tend to accept more coupons as compared to other age groups.
* Drivers with bachelors degree or no degree are equally likly to accept coupons as compared to other education background drivers.
* Income range $25k to $37.5k tend to accept more coupons as comapred to other income groups.
* Married partner tend to accept more coupons followed by singles.
<br>
<br>

## Recommendations

Based on analysis of customer behavior to accept for Bar and Coffee House coupons acceptance, I would recommend below next steps to further help understand the dataset and customer behavior.

### **A/B Test:** 
Perform A/B test with various coupon offers like bigger doiscounts on a rainy or snowy day or increasing younger customer reach out for Bar coupons.

### **Segments Trend Analysis:** 
Perform deeper segments (weather, age, gender, income etc) analysis and impact of one or more segments over other to fin tune coupons design and distribution strategy.

### **Feedback Loop:** 
Collect feedback from drivers via a well defined feedback loop to collect more data based on customer behavior and hence develop better insight into understanding the customers and coupons acceptance.

### **Businesss Colloboration:** 
Colloborate with businesses to design attractive coupons based on data collected and inferences from customer segmentation analysis.

### **ROI Reporting:** 
Develop tools to generate ROI reports which would be another input for our model to help design coupons based on demand or other customer behavior cues.




