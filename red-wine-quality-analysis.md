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

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">The dataset consists of 1,599 observations of red wine, with 12 variables.</div>

<div style="margin-top: 10px;"></div>

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

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold;">Data Exploration</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Descriptive Statistics</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
<table style="width:100%; border-collapse: collapse; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
    <thead>
      <tr style="background-color: #f2f2f2;">
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
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">A correlation analysis was conducted to assess the relationship between each variable and wine quality. Among different regressors, density was removed as it is highly correlated with fixed.acidity (-0.79) and alcohol (0.76).</div>



