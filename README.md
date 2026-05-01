# Customer-Segmentation-to-Reduce-Marketing-Wastage
FMCG Consumer Insight Case Study Using SQL and Excel

This project analyzes customer purchase behavior, campaign response, channel preference, and discount sensitivity using the Kaggle Customer Personality Analysis dataset.

The business goal is to answer a practical marketing question:

Who should we target, where should we target them, and what offer should we use to reduce ad wastage and improve campaign ROI?

Instead of targeting every customer with the same campaign, this project creates three actionable customer personas and recommends a more efficient targeting strategy.

Dataset
Source: Kaggle Customer Personality Analysis
Dataset: https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis

The dataset includes customer demographics, product spending, channel purchases, web visits, discount purchases, and historical campaign responses.

Key fields used:

Category	Variables
Demographics	Year_Birth, Education, Marital_Status, Income, Kidhome, Teenhome
Product Spend	MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds
Channel Behavior	NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth
Promotion Behavior	NumDealsPurchases
Campaign Response	AcceptedCmp1 to AcceptedCmp5, Response
Engagement	Recency
Tools Used
SQL / SQLite: data cleaning, feature engineering, persona scoring, summary tables
Excel: dashboarding, charts, review, and presentation
GitHub README visuals: chart images generated from SQL outputs
No Python or machine learning model is required for the final analysis. The segmentation uses transparent business rules, which makes it easy to explain in interviews.

Business Questions
Which customer personas are most valuable for future campaigns?
Which personas are most likely to waste advertising budget?
Which channel should each persona be targeted through?
Which personas are most discount-sensitive?
What campaign strategy should be used for each persona?
Methodology
1. Feature Engineering
Several customer-level metrics were created in SQL:

Metric	Definition	Purpose
Total_Spend	Sum of all product category spend	Measures customer value
Total_Purchases	Web + catalog + store purchases	Measures buying frequency
Deal_Share	Deal purchases / total purchases	Measures discount sensitivity
Web_Share	Web purchases / total purchases	Measures digital purchase preference
Catalog_Share	Catalog purchases / total purchases	Measures catalog preference
Store_Share	Store purchases / total purchases	Measures store preference
Any_Campaign_Response	1 if customer accepted any campaign	Measures campaign responsiveness
2. Persona Scoring
Customers were assigned to one of three personas using SQL scoring rules.

Persona	Scoring Logic
Premium Omnichannel Buyers	High spend, high purchases, stronger store/catalog behavior, campaign response
Deal-Driven Digital Browsers	High deal purchases, high web visits, stronger web behavior
Low-Engagement Occasional Buyers	Low spend, low purchases, high recency, weak campaign response
This rule-based approach was chosen because it is easy to audit, explain, and translate into campaign actions.

Persona Summary
Persona	Customer Count	Avg Total Spend	Avg Purchases	Avg Income	Campaign Response Rate
Premium Omnichannel Buyers	925	1193.46	19.33	70724.93	42.5%
Deal-Driven Digital Browsers	435	358.05	11.75	44634.25	32.4%
Low-Engagement Occasional Buyers	853	98.05	5.64	36064.60	8.2%


Insight: Premium Omnichannel Buyers are the highest-value segment by a large margin. They should be the first priority for future campaigns.

Campaign Response Analysis
Persona	Campaign Response Rate	Avg Accepted Campaigns
Premium Omnichannel Buyers	42.5%	0.79
Deal-Driven Digital Browsers	32.4%	0.40
Low-Engagement Occasional Buyers	8.2%	0.10


Insight: Premium Omnichannel Buyers are both high-value and more responsive, making them the strongest campaign target. Low-Engagement Occasional Buyers show very weak response and should not receive expensive broad campaigns.

Channel Preference Analysis
Persona	Avg Web Purchases	Avg Catalog Purchases	Avg Store Purchases	Strongest Channel
Premium Omnichannel Buyers	5.57	5.17	8.59	Store
Deal-Driven Digital Browsers	5.29	1.56	4.90	Web
Low-Engagement Occasional Buyers	1.86	0.53	3.25	Store


Insight: Premium buyers are strong across channels, especially store and catalog. Deal-Driven Digital Browsers show the strongest web orientation, so digital retargeting and email are better fits for them.

Discount Sensitivity Analysis
Persona	Avg Deal Purchases	Deal Purchase Share	Avg Total Spend	Campaign Response Rate
Deal-Driven Digital Browsers	4.07	37.7%	358.05	32.4%
Low-Engagement Occasional Buyers	1.71	32.7%	98.05	8.2%
Premium Omnichannel Buyers	2.07	11.2%	1193.46	42.5%


Insight: Deal-Driven Digital Browsers care most about discounts. They can be targeted with offers, but discount depth should be controlled to protect margin.

ROI Proxy
The dataset does not include advertising cost, so a simple value proxy was created:

Response Value Index = Average Total Spend x Campaign Response Rate

Persona	Avg Total Spend	Campaign Response Rate	Response Value Index
Premium Omnichannel Buyers	1193.46	42.5%	507.22
Deal-Driven Digital Browsers	358.05	32.4%	116.01
Low-Engagement Occasional Buyers	98.05	8.2%	8.04


Insight: Premium Omnichannel Buyers have the strongest ROI potential because they combine high spend with the strongest campaign response.

Final Targeting Matrix
Persona	Who to Target?	Where to Target?	What Offer to Use?	ROI / Wastage View
Premium Omnichannel Buyers	First priority	Store, catalog, email/web retargeting	Premium bundles, loyalty rewards, early access	Best ROI potential
Deal-Driven Digital Browsers	Secondary priority	Web, email, digital retargeting	Limited-time coupons, value packs, capped discounts	Medium ROI with margin risk
Low-Engagement Occasional Buyers	Low priority	Low-cost email only	Win-back offer only	Highest ad wastage risk
Key Recommendation
To reduce marketing wastage, campaigns should not target all customers equally.

The recommended strategy is:

Prioritize Premium Omnichannel Buyers for premium campaigns because they have the highest spend and strongest response rate.
Target Deal-Driven Digital Browsers selectively through web/email channels with controlled discounts.
Suppress Low-Engagement Occasional Buyers from expensive paid campaigns and use only low-cost reactivation tactics.
Project Files
File / Folder	Description
sql/01_build_personas_sqlite.sql	Main SQL workflow for cleaning, scoring, and exporting persona tables
sql/02_analysis_queries.sql	Additional SQL queries for insight generation
output/	CSV outputs created by SQL
outputs/customer_segmentation_completed_dashboard.xlsx	Completed Excel dashboard
outputs/customer_segmentation_excel_template.xlsx	Excel template and formula guide
figures/	README chart visuals
reports/case_study.md	Longer case study write-up
reports/linkedin_project_summary.md	LinkedIn-ready project summary
How to Run
Download the dataset from Kaggle.
Save the file as:
data/marketing_campaign.csv
Run the SQL workflow:
sqlite3 output/customer_segmentation.db < sql/01_build_personas_sqlite.sql
Open the completed Excel dashboard:
outputs/customer_segmentation_completed_dashboard.xlsx
Portfolio Summary
This project demonstrates how SQL and Excel can be used to turn raw customer data into practical marketing recommendations. By combining segmentation, campaign response analysis, channel behavior, and discount sensitivity, the analysis identifies which customers to prioritize, which channels to use, and which offers are most appropriate for each persona.

The final recommendation is to focus campaign investment on high-value omnichannel customers, use controlled digital offers for deal-sensitive customers, and reduce ad spend on low-engagement customers.
