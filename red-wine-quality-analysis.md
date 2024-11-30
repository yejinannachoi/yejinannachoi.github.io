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
  <div class="row" style="margin-bottom: 10px;">
    <div class="col-12">
      <img src="{{ site.baseurl }}/red-wine-quality-analysis/img.jpg" alt="Red Wine" class="img-fluid" style="max-width: 100%; width: 700px; display: block;">
    </div>
  </div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">Photo by <a href="https://pixabay.com/photos/wine-retro-wine-glass-wine-bottle-2408620" style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">WolfBlur on Pixabay</a></div>

<!-- ------------------------------------------- Overview ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Overview</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">This project investigates the determining factors that influence the quality of Portuguese Vinho Verde wine. Using the Red Wine Quality dataset from Kaggle, a multiple linear regression (MLR) model was developed to identify the key predictors of wine quality, and then the fit and assumptions of the model were evaluated. This research provides insights for winemakers and consumers seeking high-quality wines.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Motivation</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Wine quality has been a topic of interest for winemakers and wine enthusiasts for centuries. While many factors influence the quality of wine, the specific factors that affect overall quality remain unclear. Understanding these factors is crucial for winemakers to produce high-quality wines and for consumers to make informed choices when choosing wines.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Background</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Numerous published articles and studies on wine production and quality provide valuable insights into this topic. For instance, the book <em>Wine Production and Quality</em> by Keith Grainger highlights inconsistencies in the evaluation and description of wine quality. The absence of a universal definition of a <strong>good</strong> wine is attributed to varying standards and individual tastes within the wine industry.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">While chemical and microbiological methods can assess a wine’s technical superiority, these methods may not always align with the sensory experience of taste. However, a wine with technical imperfections may exhibit unique and authentic characteristics that evoke strong emotional responses. There is a need to identify key factors that contribute to the perceived quality of wine, and this project seeks to address that gap by investigating the determinants of wine quality using a comprehensive dataset.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Objective</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The underlying theory of this project is that the various characteristics of red wine contribute to its overall quality. The focus is on predicting red wine quality based on a set of measurable factors.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">The hypothesis is that there exists a significant linear relationship between the independent variables and the dependent variable, wine quality.</div>

<!-- ------------------------------------------- Dataset Description ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Dataset Description</div>
<div class="row" style="margin-bottom: 10px;">
<div>
      <img src="{{ site.baseurl }}/red-wine-quality-analysis/kaggle.png" alt="Kaggle" class="img-fluid" style="max-width: 100%; width: 800px;">
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
    <li>quality - a rating of the wine's quality, based on sensory data (score between 0 and 10).</li>
    </ul>
</div>

<!-- ------------------------------------------- Data Exploration ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Data Exploration</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Descriptive Statistics</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
<table style="width:100%; border-collapse: collapse; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px; text-align: center;">
    <tbody>
      <tr style="background-color: #f2f2f2;">
        <td style="border: 1px solid #ddd; padding: 8px;"> </td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>Mean (M)</strong></td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>Median (Mdn)</strong></td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>Standard Deviation (s.d.)</strong></td>
      </tr>
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
<div class="container">
  <div class="row" style="margin-bottom: 10px;">
    <div class="col-12">
  <img src="{{ site.baseurl }}/red-wine-quality-analysis/correlation-matrix.png" alt="Correlation Matrix" class="img-fluid" style="max-width: 100%; width: 600px;">
    </div>
  </div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">A correlation analysis was conducted to assess the relationship between each variable and wine quality. Among different regressors, density was removed as it is highly correlated with fixed.acidity (-0.79) and alcohol (0.76).</div>

<!-- ------------------------------------------- Model Development ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Model Development</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Multiple Linear Regression Model</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <em>quality</em>&ensp;=&ensp;β<sub>0</sub>&ensp;+&ensp;β<sub>1</sub> <em>fixed.acidity</em>&ensp;+&ensp;β<sub>2</sub> <em>volatile.acidity</em>&ensp;+&ensp;β<sub>3</sub> <em>citric.acid</em>&ensp;+&ensp;β<sub>4</sub> <em>residual.sugar</em>&ensp;+&ensp;β<sub>5</sub> <em>chlorides</em>&ensp;+&ensp;β<sub>6</sub> <em>free.sulfur.dioxide</em>&ensp;+&ensp;β<sub>7</sub> <em>total.sulfur.dioxide</em>&ensp;+&ensp;β<sub>8</sub> <em>pH</em>&ensp;+&ensp;β<sub>9</sub> <em>sulphates</em>&ensp;+&ensp;β<sub>10</sub> <em>alcohol</em>&ensp;+&ensp;<em>u</em><sub>i</sub>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Estimation Results</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 5px;">
  <table style="width:100%; border-collapse: collapse; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px; text-align: center;">
    <tbody>
      <tr style="background-color: #f2f2f2;">
        <td style="border: 1px solid #ddd; padding: 8px;"> </td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>Estimated Coefficient (β<sub>n</sub>)</strong></td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>Standard Error (SE)</strong></td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>t-value</strong></td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>p-value</strong></td>
      </tr>
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
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">* Significant at the 10% level; ** Significant at the 5% level; *** Significant at the 1% level.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Confidence Intervals (95%)</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">
  <table style="width:100%; border-collapse: collapse; font-family: 'Source Sans 3', sans-serif; margin-top: 20px; text-align: center;">
    <tbody>
      <tr style="background-color: #f2f2f2;">
        <td style="border: 1px solid #ddd; padding: 8px;"> </td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>2.5%</strong></td>
        <td style="border: 1px solid #ddd; padding: 8px;"><strong>97.5%</strong></td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">intercept</td>
        <td style="border: 1px solid #ddd; padding: 8px;">3.25</td>
        <td style="border: 1px solid #ddd; padding: 8px;">5.66</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">fixed.acidity</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.02</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.04</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">volatile.acidity</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-1.33</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.86</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">citric.acid</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.47</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.11</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">residual.sugar</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.01</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.03</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">chlorides</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-2.73</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-1.09</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">free.sulfur.dioxide</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.01</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">total.sulfur.dioxide</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.00</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">pH</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.81</td>
        <td style="border: 1px solid #ddd; padding: 8px;">-0.20</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">sulphates</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.68</td>
        <td style="border: 1px solid #ddd; padding: 8px;">1.11</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 8px;">alcohol</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.26</td>
        <td style="border: 1px solid #ddd; padding: 8px;">0.33</td>
      </tr>
    </tbody>
  </table>
</div>

<!-- ------------------------------------------- Model Evaluation ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Model Evaluation</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Metrics</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 5px;"><strong>R-Squared</strong> = 0.36</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 15px;">36% of variability in wine quality is explained by the independent variables.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 5px;"><strong>Residual Standard Error</strong> = 0.65</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 15px;">The average deviation between the observed data points and the fitted regression line is 0.65 units.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;"><strong>F-Statistic</strong> = 89.43 (<em>p</em> &lt; 2.20 × 10<sup>-16</sup>)</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Residuals</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The residuals represent the differences between the observed and predicted wine quality scores.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Minimum: -2.67</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">1st Quartile: -0.37</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Median: -0.05</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">3rd Quartile: 0.46</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Maximum: 2.04</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">The residuals are symmetrically distributed with a median close to zero, supporting the assumption that the mean of residuals is zero (MLR. 4).</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Residual Plot</div>
<div class="container">
  <div class="row" style="margin-bottom: 20px;">
    <div class="col-12">
  <img src="{{ site.baseurl }}/red-wine-quality-analysis/residual-plot.png" alt="Residual Plot" class="img-fluid" style="max-width: 100%; width: 700px;">
    </div>
  </div>
</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Q-Q Plot</div>
<div class="container">
  <div class="row" style="margin-bottom: 10px;">
    <div class="col-12">
  <img src="{{ site.baseurl }}/red-wine-quality-analysis/q-q-plot.png" alt="Q-Q Plot" class="img-fluid" style="max-width: 100%; width: 700px;">
    </div>
  </div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Plotted using residuals from the regression model and normal distribution</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Scale-Location Plot</div>
<div class="container">
  <div class="row" style="margin-bottom: 10px;">
    <div class="col-12">
  <img src="{{ site.baseurl }}/red-wine-quality-analysis/scale-location-plot.png" alt="Scale-Location Plot" class="img-fluid" style="max-width: 100%; width: 700px;">
    </div>
  </div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Plotted using square root of absolute residuals against fitted values of the regression model</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Residuals vs. Leverage Plot</div>
<div class="container">
  <div class="row" style="margin-bottom: 10px;">
    <div class="col-12">
  <img src="{{ site.baseurl }}/red-wine-quality-analysis/residual-leverage-plot.png" alt="Residuals Leverage Plot" class="img-fluid" style="max-width: 100%; width: 700px;">
    </div>
  </div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">Standardized residuals plotted against leverage (how much the observation differs from other observations)</div>

<!-- ------------------------------------------- Results & Discussion ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Results & Discussion</div>
<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Coefficients</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The estimated coefficients provide insight into the effect of each variable on wine quality while holding other variables constant.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Significant Variables:</div>
<ul style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <li>volatile.acidity = -1.10, p &lt; 0.001, indicating a strong negative effect on wine quality.</li>
  <li>chlorides = -1.91, p &lt; 0.001, indicating a strong negative effect.</li>
  <li>sulphates = +0.89, p &lt; 0.001, indicating a strong positive effect.</li>
  <li>alcohol = +0.29, p &lt; 0.001, indicating a positive effect.</li>
</ul>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Non-Significant Variables:</div>
<ul style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <li>fixed.acidity, citric.acid, residual.sugar, free.sulfur.dioxide, and total.sulfur.dioxide, as their confidence intervals include zero.</li>
</ul>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">These results might suggest that winemakers should focus on optimizing sulphates and alcohol levels while reducing volatile acidity and chlorides to improve wine quality. Non-significant variables may not have a significant effect alone but could have joint effects when considered with other predictors.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">MLR Assumptions</div>
<ol style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
  <li>
    <div><strong>MLR. 3</strong> No Perfect Multicollinearity</div>
    <ul>
    <li>The correlation matrix confirmed no perfect collinearity among predictors (correlation coefficients &lt; |1|), satisfying MLR. 3.</li>
    </ul>
  </li>
  <li>
    <div><strong>MLR. 4 </strong>Residual Mean = 0 and <strong>MLR. 6</strong> Normality of Residuals</div>
    <ul>
      <li>Residual summary statistics indicate symmetry around a median close to zero, supporting that residuals have mean zero.</li>
      <li>Deviations from the reference line at the extremes (e.g., near -3 and -2) of the Q-Q plot indicate that the residuals do not follow a perfectly normal distribution.</li>
    </ul>
  </li>
  <li>
    <div><strong>MLR. 5</strong> Homoscedasticity</div>
    <ul>
      <li>The residual plot reveals that residuals are not randomly scattered around zero, suggesting a violation of the assumption of homoscedasticity. The variance of residuals changes depending on the predicted values.</li>
      <li>The scale-location plot shows a pattern among the residuals, further confirming a violation of homoscedasticity. Ideally, the residuals should be evenly spread, but this is not observed in the plot.</li>
    </ul>
  </li>
</ol>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The multiple linear regression model provides valuable insights into factors affecting red wine quality, with significant variables such as volatile acidity, chlorides, sulphates, and alcohol playing key roles. However, the model's fit and violations of MLR assumptions suggest the need for alternative methods, such as non-linear regression or machine learning, to better capture the complexity of the data.</div>

