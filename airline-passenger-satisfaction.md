---
layout: inner
title: Airline Passenger Satisfaction
permalink: /portfolio/airline-passenger-satisfaction/
---
<div class="row" style="margin-top: 50px;">

<div>
<div style="font-size:30px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Airline Passenger
Satisfaction Prediction</div>
  
<!-- ------------------------------------------- Objective and Motivation ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 20px;">Objective and Motivation</div>




<!-- ------------------------------------------- Data Understanding ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Understanding</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Source: <a href="https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction" style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">Kaggle Public Dataset - Airline Passenger Satisfaction</a></div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Summary:</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">
  <ul>
    <li>The train set contains 103,904 rows and 23 columns, and the test set contains 25,976 rows and 23 columns. The two datasets were joined and sampled for analysis.</li>
    <li>The datasets include both categorical and numerical data such as passenger demographics, inflight and external services satisfaction levels, flight information, and satisfaction status.</li>
    <li><strong>Target Variable:</strong> <code>satisfaction</code> (1: satisfied, 0: dissatisfied or neutral).</li>
  </ul>
</div>

<!-- ------------------------------------------- Data Preparation ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Preparation</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Missing Values</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The dataset contains 393 missing values out of 129,880 for <code>Arrival Delay</code>, accounting for 0.3% of the data. To handle these missing values, we replaced the missing values with the mean of <code>Departure Delay</code>, as it showed the highest correlation with <code>Arrival Delay</code> (0.96). This approach ensures the imputation of missing values is based on a relevant and highly correlated feature.</div>

<div style="margin-top: 10px;"></div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-top: 20px;">Data Leakage</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">To avoid data leakage, we excluded variables that would not be predictive at the time of the prediction. These variables include:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li>Inflight Services Satisfaction level variables.</li>
    <li>External Services Satisfaction level variables.</li>
    <li>Arrival Delay and Departure Delay times, as they are determined by post-flight factors and are not available at prediction time.</li>
  </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">After excluding the irrelevant variables, we used a subset of features that were predictive of passenger satisfaction. These features include:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <ul>
    <li>Passenger information such as <code>Gender</code> <code>Age</code> <code>Customer Type</code> <code>Type of Travel</code> and <code>Class</code></li>
    <li><code>Flight Distance</code> and <code>satisfaction</code> (the target variable)</li>
  </ul>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-top: 20px; margin-bottom: 10px;">Normalization</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Z-Score Scaling:</strong> To prepare the data for machine learning, we applied Z-score scaling to normalize the features. This step was essential, especially for models like kNN that rely on distance metrics. Z-score scaling converts numerical attributes to a standard scale (mean = 0, standard deviation = 1), ensuring that features with different units or scales (e.g., age vs. flight distance) contribute equally to the distance computation.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;"><strong>Weighted Voting:</strong> We also employed weighted voting in kNN to give more importance to the nearest neighbors, improving the model’s prediction accuracy.</div>

<!-- ------------------------------------------- Modeling ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Modeling</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">To predict passenger satisfaction, four different classification models were built and tested to identify the best performing one.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Decision Tree</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Easy to understand, implement, and use. It is computationally inexpensive and provides a simple decision boundary.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">k-Nearest Neighbors (kNN)</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Robust to noise and does not make assumptions about the data distribution. It is computationally expensive but highly flexible for complex data.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Logistic Regression</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Robust to outliers, fast to train, and has a linear decision boundary.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Naive Bayes</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Fast and simple, requiring fewer computational resources. It assumes that features are independent, which can be a limitation.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Parameter Optimization</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Nested cross-validation with 10 folds and stratified sampling was used for hyperparameter optimization, ensuring that the model's parameters are fine-tuned to achieve the best performance.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Performance Metrics</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The five metrics were used to evaluate and compare the models:</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Accuracy, Precision, Recall, F1-Score, AUC (Area Under the Curve)</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 40px;">Utilize the best performing classification model to predict passenger satisfaction, enabling airlines to implement targeted improvements and achieve business success, such as growth in customer retention and revenue.</div>

<!-- ------------------------------------------- Evaluation ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Evaluation</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Generalization Performance</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The evaluation results for the four predictive models show varying performance across different metrics. Here are the key findings:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>The Decision Tree model</strong> was the best in terms of general performance, with good accuracy and high AUC. It is also easy to understand, implement, and computationally efficient.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;"><strong>Logistic Regression</strong> achieved the best precision, which is important in this context as we want to avoid false positives (predicting satisfied passengers when they are actually dissatisfied).</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">ROC Curves</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The ROC curves further validate the performance of the models. The Decision Tree classifier performs the best, as it is positioned most to the northwest in the curve and has the largest area under the ROC curve (AUC).</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Improvement</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The predictive model provides actionable insights into passenger satisfaction before passengers begin their journey. Airlines can use the model to identify key passenger satisfaction drivers</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <ul>
    <li><code>Customer Type</code> Disloyal customers are twice as likely to be dissatisfied.</li>
    <ul>
      <li>Offer loyalty programs that build engagement through points systems, personalized newsletters, and discounts.</li>
    </ul>
    <li><code>Travel Type</code> A significant percentage (90%) of personal travelers, particularly those traveling in Economy/Eco+ class, report lower satisfaction levels. These travelers often rate inflight services such as food, drink, and baggage handling poorly.</li>
      <ul>
      <li>Offer additional value-added services, such as assisting with luggage handling or providing waste bags, to improve their travel experience</li>
      </ul>
  </ul>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Benefits</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">
  The model helps airlines
</div>
<ul>
  <li>Increase brand reputation and popularity</li>
  <li>Stand out from competitors</li>
  <li>Retain customers and improve customer loyalty</li>
</ul>

<!-- ------------------------------------------- Deployment ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Deployment</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Implementation</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The ultimate goal of this project is to find key customer satisfaction metrics that are lacking, particularly for disloyal and personal travelers. The insights derived from the satisfaction predictions can be used to inform strategic initiatives that target these customer segments.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;"><strong>Example Insight:</strong> Disloyal and personal travelers tend to rate seat comfort and food and drink the most poorly.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Strategic Initiatives</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <ul>
    <li>Seat Comfort: Identify ways to improve comfort in the economy cabin without significantly increasing costs or reducing seating capacity. For example, consider partnering with ergonomic aircraft seat makers or offering free or low-cost amenities such as neck pillows.</li>
    <li>Food and Drink: Understand which foods and drinks are most sought-after and look for opportunities to expand the offerings. This could involve enhancing the presentation, variety, or frequency of food and beverage services.</li>
  </ul>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Considerations</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Ethical Considerations:</strong> Since only basic passenger information is being collected for the predictive model, there are no major ethical concerns.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <strong>Type 1 Error (False Positive):</strong> The risk of predicting that a passenger is dissatisfied when they are actually satisfied, which could lead to unnecessary corrective actions.
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">To reduce this risk, it is recommended to increase the sample size for better statistical significance. Additionally, studying passenger behavior before, during, and after flights will help refine the model and reduce prediction errors.</div>
