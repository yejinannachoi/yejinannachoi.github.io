---
layout: inner
title: Airline Passenger Satisfaction
permalink: /portfolio/airline-passenger-satisfaction/
---
<div class="row" style="margin-top: 50px;">

<div>
<div style="font-size:30px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Airline Passenger
Satisfaction Prediction</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Objective and Motivation</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Dataset Description</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Source: <a href="https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction" style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">Kaggle Public Dataset - Airline Passenger Satisfaction</a></div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Summary:</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <ul>
    <li>The train set contains 103,904 rows and 23 columns, and the test set contains 25,976 rows and 23 columns. The two datasets were joined and sampled for analysis.</li>
    <li>The datasets include both categorical and numerical data such as passenger demographics, inflight and external services satisfaction levels, flight information, and satisfaction status.</li>
    <li><strong>Target Variable:</strong> <code>satisfaction</code> (1: satisfied, 0: dissatisfied or neutral).</li>
  </ul>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Preprocessing</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Handling Missing Values</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The dataset contains 393 missing values out of 129,880 for <code>Arrival Delay</code>, accounting for 0.3% of the data. To handle these missing values, we replaced the missing values with the mean of <code>Departure Delay</code>, as it showed the highest correlation with <code>Arrival Delay</code> (0.96). This approach ensures the imputation of missing values is based on a relevant and highly correlated feature.</div>



<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Excluding Irrelevant Variables</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">To avoid data leakage, we excluded variables that would not be predictive at the time of the prediction. These variables include:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li>Inflight Services Satisfaction level variables.</li>
    <li>External Services Satisfaction level variables.</li>
    <li>Arrival Delay and Departure Delay times, as they are determined by post-flight factors and are not available at prediction time.</li>
  </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Data Leakage Management</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">After excluding the irrelevant variables, we used a subset of features that were predictive of passenger satisfaction. These features include:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li>Passenger information such as <code>Gender</code>, <code>Age</code>, <code>Customer Type</code>, <code>Type of Travel</code>, and <code>Class</code>.</li>
    <li><code>Flight Distance</code> and <code>satisfaction</code> (the target variable).</li>
  </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Normalization</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Z-Score Scaling:</strong> To prepare the data for machine learning, we applied Z-score scaling to normalize the features. This step was essential, especially for models like KNN that rely on distance metrics. Z-score scaling converts numerical attributes to a standard scale (mean = 0, standard deviation = 1), ensuring that features with different units or scales (e.g., age vs. flight distance) contribute equally to the distance computation.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Weighted Voting:</strong> We also employed weighted voting in KNN to give more importance to the nearest neighbors, improving the model’s prediction accuracy.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Evaluation</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Deployment</div>

</div>
