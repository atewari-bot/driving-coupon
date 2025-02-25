# Assignment 5.1 - Will the Customer Accept the Coupon?

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those who did not.

[Link to Coupons Dataset](https://github.com/atewari-bot/driving-coupon/blob/main/data/coupons.csv)

[Link to Jupyter Notebook](https://github.com/atewari-bot/driving-coupon/blob/main/driving-coupon-eda.ipynb)

## Exploratory Data Analysis (EDA)

### Missing data handling

* <b><i>car</i></b> column:
  * More than 99% of values are missing.
  * Car column have more than 99% of values missing. The type of vehicle should not affect coupon acceptance. We could drop the car column or fill it with a value 'car'. I would drop the column as this column is agnostic of coupon acceptance with 99% missing values. 
* <b><i>Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, Restaurant20To50</i></b> columns:
  * Missing values in the range of 1% to 2%.
  * We replaced null values with mode of the column.

### Fix column name
* <b><i>passanger</i><b> column: Fixed typo of column name to correct spelling <i>passenger</i>

## General data distribution visualization

### Overall Coupon Accenptance Porportion 
![Image](/images/coupons_acceptance_proportion.png)

**Key Takeaways:** 
* Overall coupons acceptance is at 56.84 %.


### Overall Coupon Type Acceptance Porportion
![Image](/images/coupons_types_distribution.png)

<table>
    <tr>
        <th>Coupon Type</th>
        <th>Total Coupon Count</th>
        <th>Accepted Coupon Count</th>
        <th>Acceptance Proportion (%)</th>
    </tr>
        <td>Bar</td>
        <td>2017</td>
        <td>827</td>
        <td>41.00</td>
    <tr>
        <td>Carry out & Take away</td>
        <td>2393</td>
        <td>1760</td>
        <td>73.55</td>
    </tr>
    <tr>
        <td>Coffee House</td>
        <td>3996</td>
        <td>1995</td>
        <td>49.92</td>
    </tr>
    <tr>
        <td>Restaurant(20-50)</td>
        <td>1492</td>
        <td>658</td>
        <td>44.10</td>
    </tr>
    <tr>
        <td>Restaurant(&lt;20)</td>
        <td>2786</td>
        <td>1970</td>
        <td>70.71</td>
    </tr>
</table>
         
**Key Takeaways:** 
* Most number of coupons distribution was for Coffee House and least number was for Restaurant(20-50).
* Carry out & Take away has highest percentage of coupon acceptance.
* Bar coupons have the lowest percentage of coupon accentance.

### Coupon acceptance by Weather
![Image](/images/temperature_histogram.png)

**Key Takeaways:** 
* Sunny day has most number of coupons acceptance

**Segments-wise Acceptance Comparision:** 
* In general, customers who visits bar more than once a month are inclined to accept bar coupons on a sunny day with an acceptance rate of 66.17 % and male drivers tend to accept more bar coupons.

![Image](/images/bar_subplots.png)
<br>
<br>

**Segment-wise Acceptance Trend:**
* Sunny weather is most preferred day for accepting coffee house coupons with acceptance rate of 66.17% compared to other weather conditions.
* Male drivers tend to accept more coupons than female drivers with an acceptance rate of 60.74%.
* Age range 21-30 tend to accept more bar coupons as compared to other age groups.
* Drivers with bachelors degree or no degree are equally likly to accept bar coupons as compared to other education background drivers.
* Income range $25k to $37.5k tend to accept more coupons as comapred to other income groups.
* Married partner highly likely to accept bar coupons compared to drivers with other marital status.


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

**Overall Acceptance:** 
* Overall 49.92% drivers accepted Coffee House coupon. This indicates there is a significant liklihood and opportunity to attract more customers by designing coupons based on deeper understanding of customer behavior and colloborating with businesses.
<br>
<br>
![Image](/images/ch_drivers_comparision.png)

**Segments-wise Acceptance Comparision:** 
* In general, customers who visits coffee house more than once a month are inclined to accept coffee house coupons on a sunny day with an acceptance rate of 63.02 %.
<br>
<br>
![Image](/images/coffee_house_subplots.png)

**Segment-wise Acceptance Trend:**
* Sunny weather is most preferred day for accepting coffee house coupons with acceptance rate of 87.26% compared to other weather conditions.
* Female drivers tend to accept more coupons than male drivers with an acceptance rate of 52.91%.
* Age range 21-26 tend to accept more coupons as compared to other age groups.
* Drivers with bachelors degree or no degree are equally likly to accept coupons as compared to other education background drivers.
* Income range $25k to $37.5k tend to accept more coupons as comapred to other income groups.
* Married partner and single are equally likely to accept more coupons compared to drivers with other marital status.
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




