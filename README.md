# Predicting and Preventing Car Accidents in Chicago

<img src="https://media.istockphoto.com/photos/chicago-cityscape-lake-michigan-at-night-picture-id1061183982?k=20&m=1061183982&s=612x612&w=0&h=ce_C2_2ZEqxjApQRhVJzAAgHcyJ8XlVD_nDuFS9Xodo=" alt="alt text" width="1000" height="450"><br>
<sup> Image courtesy of [iStock](https://www.istockphoto.com/search/2/image?phrase=chicago+skyline)<sub>
  
# Overview
We looked at data from the [Chicago Data Portal](https://data.cityofchicago.org/), specifically on [reported car accidents](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if) within the city. We stratified the data to begin from Jan 1, 2019 through Sep 12, 2021 (the most recent update from when we pulled the data).<br>
  
Our final data frame contained about 270,000 records to analyze.
  
# Business Problem
### The Chicago City Council wants to reduce the number of serious accidents in their city.<br>
  Can we build a model predicting the worst accidents there?<br>
  
# Select the target and features<br>
  * We used injuries_total as a categorical (1 indicating an injury in the accident, 0 indicating none) column as our target.<br>
  * We selected features through trial and error and basic correlation.<br>
### Features Used:<br>
  * Road defect
  * Rush hour or not
  * Crash type
  * Weather Condition
  * Simple reason for crash<br>

# Initial findings
  * About 36% of all accidents occur during reekday rush hour.
  * Certain roads have defects that lead to more accidents, with the main offender being Western Ave (see below).
  * Disobeying the rules of the road, along with drug/alcohol abuse, lead to most accidents that result in injury.<br>
  
<img src="images/chitown_map.png" align="center"><br>
  
The above image highlights accidents caused by defects in the road. The main offenders are:<br>
  * Western Ave
  * Ashland Ave
  * Halsted St
  * Cicero Ave
  * Lake Shore Dr NB<br>

<img src="images/rush_hour_time_of_week.png" align="center"><br>
The pie chart on the left shows the amount of accidents that occur during weekday rush hour. The one on the right shows how many hours of rush hour take up each week.<br>
  
<img src="images/rush_hour_chart.png" align="center"><br>
About 45% of weekday accidents occur during rush hour.
  
<img src="images/accident_driver_causes.png" align="center"><br>
The largest cause of accidents in general is reckless/poor driving and decision making (poor lane changes, etc.)<br>

<img src="images/accidents_by_injury.png" align="center"><br>
However, most injuries in accidents were drug/alcohol related and due to breaking the rules of the road (running a stop sign, etc.)<br>
  
<img src="images/model_matrices.PNG" align="center"><br>
We created a baseline model on the left which did a poor job predicting injury results (1 = injury, 0 = no injury).<br>
Our second model, on the right, did a much better job using Recall as the underlying metric.<br>
  
Our recommendations include:<br>
  * More visible/obvious traffic signs
  * Increase the delay between the red and green light
  * More resources towards drunk driving prevention and education
  * Quicker maintenance on most frequently used roads
  * Create safer and more reliable rush hour commuting environments and transportation options
  * Increase number of first aid responders on-duty during these times

