# A-B-Testing-Marketing-Campaign-Performance-Social-Media-vs-Email

This project performs a complete, end-to-end A/B test to determine which marketing channel — Social Media or Email Marketing — delivers a higher conversion rate for a digital marketing campaign.

The experiment uses real-world digital marketing metrics such as ad spend, click-through rate, website visits, email engagement, and customer purchase behavior.

###### 1. Business Question
Which marketing channel produces a higher conversion rate:
Social Media or Email Marketing?

The company wants to ensure that any marketing budget reallocation is based on statistically valid evidence, not assumptions.

###### 2. Experiment Goal
Increase user conversion (binary variable: 1 = converted, 0 = not converted) by choosing the best-performing marketing channel based on statistical testing.

###### 3. Hypotheses
* Null Hypothesis (H₀)
There is no difference in conversion rates:
Conversion_A = Conversion_B
Alternative Hypothesis (H₁)
* There is a difference in conversion rates:
Conversion_A ≠ Conversion_B
This is a two-sided hypothesis test.

4. Metrics
######  Primary Metric
* Conversion Rate (CR) = conversions ÷ total users

######  Secondary Metrics
* EmailOpens
* EmailClicks
* AdSpend per conversion
* Engagement metrics: TimeOnSite, WebsiteVisits
* Customer value metrics: LoyaltyPoints, PreviousPurchases
* These ensure there are no negative side effects from the treatment.

5. Dataset Overview
* Total rows: 8,000
* Columns: 20
###### Key variables used:
* Column	Description
* CampaignChannel	Social Media or Email
* Conversion	Primary outcome (1/0)
* AdSpend	Marketing spend per user
* ClickThroughRate	Ad engagement
* EmailOpens / EmailClicks	Email engagement
* WebsiteVisits / TimeOnSite	User behavior
* Income, Age, Gender	Covariates for balance check

6. Experiment Design
* Group A: Social Media
* Group B: Email
* Significance level: α = 0.05
* Power: 80%
* Minimum Detectable Effect (MDE): 5% absolute difference

###### Pre-experiment checks:
* Sample balance checks
* Covariate distribution similarity
* Required sample size (≈586 per group)
* The dataset already satisfies sample-size requirements.

7. Statistical Testing
###### Test Used:
* Two-sided z-test for difference in proportions
* Results Summary
* Metric	Social Media	Email
* Conversion Rate	86.83%	87.03%
* Lift (Email – Social Media)	+0.19%	
* 95% CI	[-2.19%, +2.58%]	
* p-value	0.8739	

###### Interpretation:
There is no statistically significant difference between Social Media and Email. We fail to reject H₀.
* Model Validation (Logistic Regression)
* A regression model controlling for Age, Income, Gender confirms:
* Channel effect is not significant (p = 0.784)
* Results are consistent with the z-test

8. Cost Analysis
Channel	Total Spend	Conversions	Cost per Conversion
* Email	$7.87M	1355	$5809
* Social Media	$7.54M	1319	$5718

Social Media is slightly more cost-efficient, despite similar conversion rates.

9. Secondary Metrics Check

###### Among converted users:
* Income, PreviousPurchases, and LoyaltyPoints are similar.
* No evidence of harmful quality effects.
* Email attract slightly lower-income customers on average.
* No negative side-effects detected.


10. Conclusion & Recommendation
* No statistically significant difference in conversion rate between Social Media and Email.
* Social Media has lower cost per conversion, making it more cost-efficient.

Recommendation:
* Maintain both channels, but shift marginal budget toward Social Media for better ROI — unless future experiments show otherwise.

11. Extensions / Future Work
* A/B test CampaignType (Awareness vs Conversion campaigns)
* Multi-armed bandit to optimize budget allocation
* Incrementality testing with geo-holdouts
* Customer lifetime value (CLV) comparison by channel


12. Technologies Used
* Python
* Pandas, NumPy
* Statsmodels
* Matplotlib
* Jupyter Notebook

 Author

James Kingsley Philip
Data Scientist & Data Engineer
