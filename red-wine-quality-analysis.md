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
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;"><strong>Input Variables:</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
    <ul>
      <li>fixed.acidity: the amount of fixed acids (non-volatile) in the wine</li>
      <li>volatile.acidity: the amount of volatile acids (acetic acid) in the wine</li>
      <li>citric.acid: the amount of citric acid in the wine</li>
      <li>residual.sugar: the amount of residual sugar (unfermented sugar) in the wine</li>
      <li>chlorides: the amount of salt in the wine</li>
      <li>free.sulfur.dioxide: the amount of free form of sulfur dioxide in the wine</li>
      <li>total.sulfur.dioxide: the total amount of sulfur dioxide in the wine, including both free and bound
forms</li>
      <li>density: the density of the wine</li>
      <li>pH: the pH level of the wine, on a scale from 0 (very acidic) to 14 (very basic)</li>
      <li>sulphates: the amount of sulphates in the wine</li>
      <li>alcohol: the alcohol content of the wine (in %)</li>
  </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;"><strong>Input Variables:</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">
    <ul>
    <li>quality: a rating of the wine's quality, based on sensory data, score between 0 and 10.</li>
    </ul>
</div>
    
