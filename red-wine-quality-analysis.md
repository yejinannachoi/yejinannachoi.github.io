---
layout: inner
title: Red Wine Quality Prediction
permalink: /portfolio/red-wine-quality-analysis/
---
<div class="container" style="margin-top: 50px;">

  <!-- Title Section -->
  <div class="row">
    <div class="col-12">
      <div style="font-size:40px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">
        Red Wine Quality Analysis
      </div>
    </div>
  </div>

  <!-- Tags Section -->
  <div class="row" style="margin-bottom: 20px;">
    <div class="col-12">
      <div class="tags-container" style="display: flex; gap: 10px; flex-wrap: wrap;">
        <span class="tag r">R</span>
        <span class="tag multiple-linear-regression">Multiple Linear Regression</span>
      </div>
    </div>
  </div>

  <!-- Image Section -->
  <div class="row" style="margin-bottom: 40px;">
    <div class="col-12">
      <img src="{{ site.baseurl }}/airline-passenger-satisfaction/img.jpg" alt="Aircraft" class="img-fluid" style="max-width: 100%; width: 700px; display: block;">
    </div>
  </div>
</div>

<!-- ------------------------------------------- Overview ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Overview</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">This project investigates the determining factors that influence the quality of Portuguese Vinho Verde wine. Using the Red Wine Quality dataset from Kaggle, we developed a multiple linear regression (MLR) model to identify the key predictors of wine quality and evaluated the fit and assumptions of the model. This research provides insights for winemakers and consumers seeking high-quality wines.</div>

<!-- ------------------------------------------- Dataset Description ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Dataset Description</div>
<div class="row" style="margin-bottom: 10px;">
<div>
      <img src="{{ site.baseurl }}/airline-passenger-satisfaction/kaggle.png" alt="Kaggle" class="img-fluid" style="max-width: 100%; width: 800px;">
</div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">Source: <strong><a href="https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009" style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">Kaggle Public Dataset - Red Wine Quality</a></strong></div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The dataset consists of 1,599 observations of red wine, with 12 variables.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;"><strong>Input Variables:</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
    <ul>
      <li>fixed.acidity - the amount of fixed acids (non-volatile) in the wine</li>
      <li>volatile.acidity - the amount of volatile acids (acetic acid) in the wine</li>
      <li>citric.acid - the amount of citric acid in the wine</li>
      <li>residual.sugar - the amount of residual sugar (unfermented sugar) in the wine</li>
      <li>chlorides - the amount of salt in the wine</li>
      <li>free.sulfur.dioxide - the amount of free form of sulfur dioxide in the wine</li>
      <li>total.sulfur.dioxide - the total amount of sulfur dioxide in the wine, including both free and bound
forms</li>
      <li>density - the density of the wine</li>
      <li>pH - the pH level of the wine, on a scale from 0 (very acidic) to 14 (very basic)</li>
      <li>sulphates - the amount of sulphates in the wine</li>
      <li>alcohol - the alcohol content of the wine (in %)</li>
  </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;"><strong>Output Variable:</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">
    <ul>
    <li>quality - a rating of the wine's quality, based on sensory data, score between 0 and 10.</li>
    </ul>
</div>

<!-- ------------------------------------------- Data Exploration ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Exploration</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Descriptive Statistics</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
<table style="width:100%; border-collapse: collapse; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px; text-align: center;">
    <thead>
      <tr style="background-color: #f2f2f2; text-align: center;">
        <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">Variable</th>
        <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">Mean (M)</th>
        <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">Median (Mdn)</th>
        <th style="border: 1px solid #ddd; padding: 8px; text-align: left;">Standard Deviation (s.d.)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">fixed.acidity</td>
        <td style="border: 1px solid #ddd; padding: 8px;">8.32</td>
        <td style="border: 1px solid #ddd; padding: 8px;">7.90</td>
        <td style="border: 1px solid #ddd; padding: 8px;">1.74</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">volatile.acidity</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.53</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.52</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.18</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">citric.acid</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.27</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.26</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.19</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">residual.sugar</td>
        <td style="border: 1px solid #ddd; padding: 8px;">2.54</td>
        <td style="border: 1px solid #ddd; padding: 8px;">2.20</td>
        <td style="border: 1px solid #ddd; padding: 8px;">1.41</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">chlorides</td>
        <td style="border: 1px solid #ddd; padding: 8px;">8.75 × 10<sup>-2</sup></td>
        <td style="border: 1px solid #ddd; padding: 8px;">7.90 × 10<sup>-2</sup></td>
        <td style="border: 1px solid #ddd; padding: 8px;">4.71 × 10<sup>-2</sup></td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">free.sulfur.dioxide</td>
        <td style="border: 1px solid #ddd; padding: 8px;">15.87</td>
        <td style="border: 1px solid #ddd; padding: 8px;">14.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">10.46</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">total.sulfur.dioxide</td>
        <td style="border: 1px solid #ddd; padding: 8px;">46.47</td>
        <td style="border: 1px solid #ddd; padding: 8px;">38.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">32.90</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">density</td>
        <td style="border: 1px solid #ddd; padding: 8px;">9.97 × 10<sup>-1</sup></td>
        <td style="border: 1px solid #ddd; padding: 8px;">9.97 × 10<sup>-1</sup></td>
        <td style="border: 1px solid #ddd; padding: 8px;">1.89 × 10<sup>-3</sup></td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">pH</td>
        <td style="border: 1px solid #ddd; padding: 8px;">3.31</td>
        <td style="border: 1px solid #ddd; padding: 8px;">3.31</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.15</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">sulphates</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.66</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.62</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.17</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">alcohol</td>
        <td style="border: 1px solid #ddd; padding: 8px;">10.42</td>
        <td style="border: 1px solid #ddd; padding: 8px;">10.20</td>
        <td style="border: 1px solid #ddd; padding: 8px;">1.07</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">quality</td>
        <td style="border: 1px solid #ddd; padding: 8px;">5.64</td>
        <td style="border: 1px solid #ddd; padding: 8px;">6.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.81</td>
      </tr>
    </tbody>
  </table>
  </div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Correlation Matrix</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">A correlation analysis was conducted to assess the relationship between each variable and wine quality. Among different regressors, density was removed as it is highly correlated with fixed.acidity (-0.79) and alcohol (0.76).</div>

<!-- ------------------------------------------- Model Development ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Model Development</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Multiple Linear Regression Model</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px; line-height: 1.6;"><em>quality</em>  = β<sub>0</sub>  + β<sub>1</sub> <em>fixed.acidity</em>  + β<sub>2</sub> <em>volatile.acidity</em>  + β<sub>3</sub> <em>citric.acid</em>  + β<sub>4</sub> <em>residual.sugar</em>  + β<sub>5</sub> <em>chlorides</em>  + β<sub>6</sub> <em>free.sulfur.dioxide</em>  + β<sub>7</sub> <em>total.sulfur.dioxide</em>  + β<sub>8</sub> <em>pH</em>  + β<sub>9</sub> <em>sulphates</em>  + β<sub>10</sub> <em>alcohol</em>  + <em>u</em><sub>i</sub></div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Estimation Results</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 5px; line-height: 1.6;">
  <table style="width:100%; border-collapse: collapse; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px; text-align: center;">
    <thead>
      <tr style="background-color: #f2f2f2; text-align: center;">
        <th style="border: 1px solid #ddd; padding: 8px;">Variable</th>
        <th style="border: 1px solid #ddd; padding: 8px;">Estimated Coefficient (β<sub>n</sub>)</th>
        <th style="border: 1px solid #ddd; padding: 8px;">Standard Error (SE)</th>
        <th style="border: 1px solid #ddd; padding: 8px;">t-value</th>
        <th style="border: 1px solid #ddd; padding: 8px;">p-value</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">intercept</td>
        <td style="border: 1px solid #ddd; padding: 8px;">4.45</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.61</td>
        <td style="border: 1px solid #ddd; padding: 8px;">7.27</td>
        <td style="border: 1px solid #ddd; padding: 8px;">5.59 × 10<sup>-13</sup> ***</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">fixed.acidity</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.01</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.02</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.51</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.61</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">volatile.acidity</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-1.10</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.12</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-9.13</td>
        <td style="border: 1px solid #ddd; padding: 8px;">&lt; 2.00 × 10<sup>-16</sup> ***</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">citric.acid</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.18</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.15</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-1.25</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.21</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">residual.sugar</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.01</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.01</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.74</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.46</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">chlorides</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-1.91</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.42</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-4.57</td>
        <td style="border: 1px solid #ddd; padding: 8px;">5.30 × 10<sup>-6</sup> ***</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">free.sulfur.dioxide</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">2.09</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.04 *</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">total.sulfur.dioxide</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-4.56</td>
        <td style="border: 1px solid #ddd; padding: 8px;">5.52 × 10<sup>-6</sup> ***</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">pH</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.50</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.16</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-3.21</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00 **</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">sulphates</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.89</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.11</td>
        <td style="border: 1px solid #ddd; padding: 8px;">8.06</td>
        <td style="border: 1px solid #ddd; padding: 8px;">1.46 × 10<sup>-15</sup> ***</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">alcohol</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.29</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.02</td>
        <td style="border: 1px solid #ddd; padding: 8px;">16.88</td>
        <td style="border: 1px solid #ddd; padding: 8px;">&lt; 2.00 × 10<sup>-16</sup> ***</td>
      </tr>
    </tbody>
  </table>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">* Significant at the 10% level; ** Significant at the 5% level; *** Significant at the 1% level.</div>


