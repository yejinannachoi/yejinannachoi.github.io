---
layout: inner
title: Shark Tank Deal Prediction
permalink: /portfolio/shark-tank-deal-prediction/
---
<div class="container" style="margin-top: 50px;">

  <!-- Title Section -->
  <div class="row">
    <div class="col-12">
      <div style="font-size:40px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">
        Shark Tank Deal Prediction
      </div>
    </div>
  </div>

  <!-- Tags Section -->
  <div class="row" style="margin-bottom: 20px;">
    <div class="col-12">
      <div class="tags-container" style="display: flex; gap: 10px; flex-wrap: wrap;">
        <span class="tag python">Python</span>
        <span class="tag machine-learning">Machine Learning</span>
        <span class="tag classification-models">Classification Models</span>
        <span class="tag supervised-learning">Supervised Learning</span>
      </div>
    </div>
  </div>

  <!-- Image Section -->
  <div class="row" style="margin-bottom: 10px;">
    <div class="col-12">
      <img src="{{ site.baseurl }}/shark-tank-deal-prediction/img.jpg" alt="Business" class="img-fluid" style="max-width: 100%; width: 700px; display: block;">
    </div>
  </div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">Photo by <a href="https://pixabay.com/photos/business-handshake-business-deal-7111770/" style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">tungnguyen0905 on Pixabay</a></div>



<!-- ------------------------------------------- Introduction  ------------------------------------------- -->

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Introduction</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Project Goal</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">On ABC’s Shark Tank, entrepreneurs have the opportunity to obtain investments for their growing companies from a panel of experienced investors, or sharks. The goal of this project is to analyze the factors that influence whether these entrepreneurs reach a deal with one of the sharks using data from previous Shark Tank pitches. Uncovering the factors that most heavily influence an entrepreneur’s success in bargaining with the sharks would allow stakeholders to predict whether a company will successfully secure a deal and offer insights into trends for emerging markets.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Implications</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">By analyzing the factors that influence successful negotiations on Shark Tank, this project provides actionable insights that benefit multiple stakeholders:</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Improve Entrepreneurship</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Entrepreneurs can gain a deeper understanding of the types of businesses, industries, and characteristics most likely to attract investors. These insights allow entrepreneurs to refine their business models and align their business strategies with investor expectations, increasing their chances of securing funding.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Drive Economic Growth</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">Businesses that secure investments generate jobs, revenue, and economic activity. By identifying the factors that lead to successful deals, this project contributes to broader economic development goals. Policymakers can leverage these insights to design initiatives that promote entrepreneurship in underrepresented industries and regions.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;"><strong>Inform Investment Decisions</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">Investors can use data-driven insights from this project to identify emerging trends and new market opportunities. Understanding the factors that lead to successful deals, such as specific industry patterns or regional strengths, enables investors to make more informed and effective investment decisions, reducing risk and increasing returns.</div>

<div style="font-size:20px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Questions</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <ul>
        <li>What types of businesses are most successful in securing deals from the Sharks?</li>
        <li>Which Sharks are most likely to invest in particular industries or types of businesses?</li>
        <li>What factors contribute to successful negotiations between entrepreneurs and the Sharks?</li>
        <li>How does the number of entrepreneurs impact the likelihood of securing a deal?</li>
        <li>How does the location of entrepreneurs and their businesses affect investment decisions?</li>
        <li>Are there patterns in the types of products or businesses pitched by entrepreneurs from different regions?</li>
    </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;">The initial hypothesis is that factors like the company’s category (i.e. industry), location, and multiple_entrepreneurs are strong predictors as to whether a company is able to reach a deal.</div>


<!-- ------------------------------------------- Dataset Overview ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Dataset Overview</div>
<div class="row" style="margin-bottom: 10px;">
<div>
      <img src="{{ site.baseurl }}/shark-tank-deal-prediction/kaggle.png" alt="Kaggle" class="img-fluid" style="max-width: 100%; width: 800px;">
</div>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">Source: <strong><a href="https://www.kaggle.com/datasets/ulrikthygepedersen/shark-tank-companies" style="font-size:16px; font-family: 'Source Sans 3', sans-serif;">Kaggle Public Dataset - Shark Tank Companies</a></strong></div>

<div style="margin-top: 10px;"></div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The dataset includes 495 rows and 19 columns, with each row representing a pitch previously aired on Shark Tank.</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;"><strong>Dependent Variable:</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
    <ul>
    <li><strong>deal</strong> - whether or not the company received a deal (target variable)</li>
    </ul>
</div>

<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif;"><strong>Independent Variables:</strong></div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">
    <ul>
        <li><strong>location</strong> - the city and state where the company is based, can impact the company’s market reach, regulatory environment, and access to resources such as talent</li>
        <li><strong>website</strong> - the company's website URL, can impact the company’s ability to provide easily accessible, important information on products or services to customers</li>
        <li><strong>askedfor</strong> - the amount of money that the entrepreneur(s) asked for in exchange for a stake in their company</li>
        <li><strong>exchangeforstake</strong> - the percentage of the company's ownership that the entrepreneur(s) offered in exchange for the investment</li>
        <li><strong>valuation</strong> - the valuation of the company at the time of its appearance on the show</li>
        <li><strong>multiple_entrepreneurs</strong> - whether or not there are multiple entrepreneurs, can impact the company’s leadership structure and decision-making process</li>
        <li>description - a brief description of the company and its products or services</li>
        <li>episode - the episode of the show</li>
        <li>category - the industry or sector in which the company operates, can impact the company’s growth potential and the level of competition</li>
        <li>entrepreneurs - the name(s) of the entrepreneur(s)</li>
        <li>season - the season of the show</li>
        <li>shark1 - the name of the 1st shark</li>
        <li>shark2 - the name of the 2nd shark</li>
        <li>shark3 - the name of the 3rd shark</li>
        <li>shark4 - the name of the 4th shark</li>
        <li>shark5 - the name of the 5th shark</li>
        <li>title - the name of the company</li>
        <li>episode_season - the episode and season of the show</li>
    </ul>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;"><em>Bolded variables were used for classification tasks, while the rest were excluded due to their lack of relevance to the target variable.</em></div>



