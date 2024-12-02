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



<!-- ------------------------------------------- Implications ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Implications</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 10px;">The primary objective of this analysis is to uncover the factors contributing to successful negotiations between entrepreneurs and the Sharks on Shark Tank.</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
<ul>
        <li><strong>Improving Entrepreneurship</strong>
            <ul>
                <li>Entrepreneurs gain actionable insights into the characteristics of pitches most likely to secure investments, such as industry focus, funding requests, and team dynamics.</li>
                <li>Understanding trends in successful businesses can help entrepreneurs refine their pitches and position their companies for growth and scalability.</li>
            </ul>
        </li>
        <li><strong>Informing Investment Decisions</strong>
            <ul>
                <li>Investors can leverage the findings to identify the industries, regions, and business models with higher success rates.</li>
                <li>By recognizing patterns in Shark Tank deals, investors can make more informed decisions, develop effective strategies, and align their portfolios with emerging market trends.</li>
            </ul>
        </li>
        <li><strong>Enhancing Negotiation Success</strong>
            <ul>
                <li>Factors such as team size and location influence the likelihood of deal success, providing entrepreneurs with insights to optimize their approach and strengthen their proposals.</li>
                <li>This knowledge can encourage entrepreneurs to address potential barriers and highlight deal-attracting aspects in their pitches.</li>
            </ul>
        </li>
        <li><strong>Supporting Economic Growth</strong>
            <ul>
                <li>Analyzing patterns in successful businesses identifies emerging markets and industries that are ripe for growth, helping policymakers craft initiatives to support entrepreneurship.</li>
                <li>Investments made in promising companies can lead to job creation, innovation, and regional economic development.</li>
            </ul>
        </li>
        <li><strong>Expanding the Investment Landscape</strong>
            <ul>
                <li>By understanding which factors consistently lead to success, the insights can encourage broader investment participation and foster collaborations between entrepreneurs and investors.</li>
                <li>Emerging markets and underrepresented industries gain visibility, driving innovation and diversification in entrepreneurial ecosystems.</li>
            </ul>
        </li>
    </ul>
</div>

<!-- ------------------------------------------- Questions ------------------------------------------- -->
<hr>

<div style="font-size:25px; font-family: 'Source Sans 3', sans-serif; font-weight: bold; margin-bottom: 10px;">Questions</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 20px;">
  <ul>
        <li><strong>Business Success:</strong> What types of businesses are most successful in securing deals from the Sharks?</li>
        <li><strong>Shark Preferences:</strong> Which Sharks are most likely to invest in particular industries or types of businesses?</li>
        <li><strong>Negotiation Factors:</strong> What specific factors contribute to successful negotiations between entrepreneurs and the Sharks?</li>
        <li><strong>Team Dynamics:</strong> How does the number of entrepreneurs impact the likelihood of securing a deal?</li>
        <li><strong>Geographical Influence:</strong> How does the location of entrepreneurs and their businesses affect investment decisions?</li>
        <li><strong>Regional Trends:</strong> Are there patterns in the types of products or businesses pitched by entrepreneurs from different regions?</li>
    </ul>
</div>


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
        <li>description - a brief description of the company and its products or services</li>
        <li>episode - the episode of the show</li>
        <li>category - the industry or sector in which the company operates, can impact the company’s growth potential and the level of competition</li>
        <li>entrepreneurs - the name(s) of the entrepreneur(s)</li>
        <li><strong>location</strong> - the city and state where the company is based, can impact the company’s market reach, regulatory environment, and access to resources such as talent</li>
        <li><strong>website</strong> - the company's website URL, can impact the company’s ability to provide easily accessible, important information on products or services to customers</li>
        <li><strong>askedfor</strong> - the amount of money that the entrepreneur(s) asked for in exchange for a stake in their company</li>
        <li><strong>exchangeforstake</strong> - the percentage of the company's ownership that the entrepreneur(s) offered in exchange for the investment</li>
        <li><strong>valuation</strong> - the valuation of the company at the time of its appearance on the show</li>
        <li>season - the season of the show</li>
        <li>shark1 - the name of the 1st shark</li>
        <li>shark2 - the name of the 2nd shark</li>
        <li>shark3 - the name of the 3rd shark</li>
        <li>shark4 - the name of the 4th shark</li>
        <li>shark5 - the name of the 5th shark</li>
        <li>title - the name of the company</li>
        <li>episode_season - the episode and season of the show</li>
        <li><strong>multiple_entrepreneurs</strong> - whether or not there are multiple entrepreneurs, can impact the company’s leadership structure and decision-making process</li>
    </ul>
</div>
<div style="font-size:16px; font-family: 'Source Sans 3', sans-serif; margin-bottom: 40px;"><em>Bolded variables were used for classification tasks, while the remaining variables were excluded due to their lack of relevance to the target variable.</em></div>



