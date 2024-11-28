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

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Understanding</div>
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

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Preparation</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Handling Missing Values</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The dataset contains 393 missing values out of 129,880 for <code>Arrival Delay</code>, accounting for 0.3% of the data. To handle these missing values, we replaced the missing values with the mean of <code>Departure Delay</code>, as it showed the highest correlation with <code>Arrival Delay</code> (0.96). This approach ensures the imputation of missing values is based on a relevant and highly correlated feature.</div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Excluding Irrelevant Variables</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">To avoid data leakage, we excluded variables that would not be predictive at the time of the prediction. These variables include:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li>Inflight Services Satisfaction level variables.</li>
    <li>External Services Satisfaction level variables.</li>
    <li>Arrival Delay and Departure Delay times, as they are determined by post-flight factors and are not available at prediction time.</li>
  </ul>
</div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Preventing Data Leakage</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">After excluding the irrelevant variables, we used a subset of features that were predictive of passenger satisfaction. These features include:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li>Passenger information such as <code>Gender</code>, <code>Age</code>, <code>Customer Type</code>, <code>Type of Travel</code>, and <code>Class</code></li>
    <li><code>Flight Distance</code> and <code>satisfaction</code> (the target variable)</li>
  </ul>
</div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Normalization</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Z-Score Scaling:</strong> To prepare the data for machine learning, we applied Z-score scaling to normalize the features. This step was essential, especially for models like KNN that rely on distance metrics. Z-score scaling converts numerical attributes to a standard scale (mean = 0, standard deviation = 1), ensuring that features with different units or scales (e.g., age vs. flight distance) contribute equally to the distance computation.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;"><strong>Weighted Voting:</strong> We also employed weighted voting in KNN to give more importance to the nearest neighbors, improving the model’s prediction accuracy.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Evaluation</div>







<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Deployment</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Implementation</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The ultimate goal of this project is to find key customer satisfaction metrics that are lacking, particularly for disloyal and personal travelers. The insights derived from the satisfaction predictions can be used to inform strategic initiatives that target these customer segments.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Example Insight</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Disloyal and personal travelers tend to rate seat comfort and food and drink the most poorly.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Strategic Initiatives</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li><strong>Seat Comfort:</strong> Identify ways to improve comfort in the economy cabin without significantly increasing costs or reducing seating capacity. For example, consider partnering with ergonomic furniture makers or offering free or low-cost amenities such as neck pillows.</li>
    <li><strong>Food and Drink:</strong> Understand which foods and drinks are most sought-after and look for opportunities to expand the offerings. This could involve enhancing the presentation, variety, or frequency of food and beverage services.</li>
  </ul>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Considerations</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Ethical Considerations:</strong> Since only basic passenger information is being collected for the predictive model, there are no major ethical concerns.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Risks</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <strong>Type 1 Error (False Positive):</strong> The risk of predicting that a passenger is dissatisfied when they are actually satisfied, which could lead to unnecessary corrective actions.
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <strong>Mitigation:</strong> To reduce this risk, it is recommended to increase the sample size for better statistical significance. Additionally, studying passenger behavior before, during, and after flights will help refine the model and reduce prediction errors.
</div>
