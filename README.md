Customer Segmentation to Reduce Marketing Wastage
SQL + Excel Consumer Insight Case Study
This project uses the Kaggle Customer Personality Analysis dataset to build customer personas and recommend more efficient campaign targeting.

The main business question is:

How can customer segmentation help reduce ad wastage and improve campaign ROI by identifying who to target, where to target them, and what offer to use?

The project is designed as a portfolio-ready case study for Market Analyst, Consumer Insight Analyst, and Consumer Behavior Analyst roles.



Executive Summary
The analysis identified three customer personas:

Persona	Customer Count	Avg Spend	Campaign Response	Main Channel Signal	Discount Sensitivity	Campaign Decision
Premium Omnichannel Buyers	925	1193.46	42.5%	Strong store/catalog behavior	11.2% deal share	Prioritize
Deal-Driven Digital Browsers	435	358.05	32.4%	Strong web behavior	37.7% deal share	Target selectively
Low-Engagement Occasional Buyers	853	98.05	8.2%	Low purchase activity	32.7% deal share	Suppress from expensive campaigns
Final recommendation:
Prioritize Premium Omnichannel Buyers for premium campaigns, target Deal-Driven Digital Browsers with controlled digital offers, and reduce spend on Low-Engagement Occasional Buyers because they show the highest ad wastage risk.




🎯 Business Goal
Reduce advertising wastage and improve ROI by identifying:
Who to target
Which channel to use
What offer to give
This project is designed for:
Market Analyst Portfolio
Consumer Insight Analyst Portfolio
Consumer Behavior Analyst Portfolio
📁 Dataset Information
Source: Kaggle Customer Personality Analysis Dataset
Link: https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis
File Path: data/marketing_campaign.csv
⚠️ Note: The dataset is usually tab-separated even if it has a .csv extension.
🧠 Business Questions
Which customer personas are most valuable for future campaigns?
Which personas waste advertising budget?
Which channel works best: web, store, or catalog?
Which personas are most discount-sensitive?
What campaign strategy should be used per persona?
👥 Persona Framework
Persona	Core Behavior	Targeting Role
💎 Premium Omnichannel Buyers	High spend, multi-channel usage	Highest priority
💻 Deal-Driven Digital Browsers	Web-heavy, discount sensitive	Secondary target
⚠️ Low-Engagement Occasional Buyers	Low spend, low activity	Suppress / minimal targeting
🧠 Segmentation Logic (Scoring Model)
Customers are scored using:
Total Spend
Purchase Frequency
Web Purchases
Store Purchases
Catalog Purchases
Deal Purchases
Campaign Response
Recency
📊 Concept Flow



📈 Analysis Modules
1. Segmentation Analysis
Feature	Description
Total Spend	Lifetime value
Web Purchases	Online behavior
Store Purchases	Offline behavior
Catalog Purchases	Catalog engagement
Deal Purchases	Discount usage
Recency	Last activity
Campaign Response	Engagement
2. Campaign Response Analysis



3. Channel Preference Analysis
Diagram is not supported.

4. Discount Sensitivity Analysis
Persona	Sensitivity	Risk
💎 Premium Buyers	Low	High value
💻 Deal Browsers	High	Margin risk
⚠️ Low Engagement	Medium	Low ROI
🎯 Recommended Strategy
Persona	Priority	Channel	Offer	ROI Impact
💎 Premium Buyers	High	Catalog / Store / Email	Loyalty rewards	High ROI
💻 Deal Browsers	Medium	Web / Email	Coupons	Medium ROI
⚠️ Low Engagement	Low	Email only	Win-back offers	High wastage risk
📉 Business Impact
Metric	Before	After
Campaign Efficiency	Low	High
Budget Waste	High	Reduced
Conversion Rate	Moderate	Improved
🚀 Tools Used
SQL (Segmentation logic)
Excel (Analysis)
Kaggle dataset
🧭 Outcome
This project converts raw customer data into:
Clear marketing personas
Targeting strategy
Reduced ad wastage
Improved ROI
⭐ Portfolio Value
Perfect for:
Marketing Analyst roles
Data Analyst roles
CRM Analyst roles
Consumer Insight rolesKey features used:
Total spend & category spend
Web, store, catalog purchases
Web visits
Deal purchases
Recency
Campaign responses
📊 Add chart here:
![Customer Segmentation](images/segmentation_chart.png)


--
2. Campaign Response Analysis
Metrics:
AcceptedCmp1–AcceptedCmp5
Overall response rate
Total accepted campaigns
📊 Add chart here:
![Campaign Response by Persona](images/campaign_response.png)


--
3. Channel Preference Analysis
Comparison across:
Web
Store
Catalog
⚠️ Note: Used as efficiency proxy, not true ROI (no cost data available)
📊 Add chart here:
![Channel Preference](images/channel_analysis.png)


--
4. Discount Sensitivity Analysis
Metrics:
Number of deal purchases
Deal share of purchases
Spend vs discount usage
📊 Add chart here:
![Discount Sensitivity](images/discount_analysis.png)


📈 Key Insights
Premium customers drive the highest value across all channels
Discount-driven users respond well but reduce margins
Low-engagement users consume budget with minimal return


--
🎯 Recommended Campaign Strategy
Persona	Who to Target	Channel	Offer Strategy	ROI View
Premium Omnichannel Buyers	First priority	Catalog, Store, Email	Loyalty rewards, premium bundles	⭐ Best ROI
Deal-Driven Digital Browsers	Secondary	Web, Email	Limited-time discounts	⚖️ Medium ROI
Low-Engagement Buyers	Avoid	Low-cost email only	Win-back offers	🚫 High wastage


--
🛠 Tools Used
SQL (segmentation & aggregation)
Excel (analysis & visualization)


--
📌 Project Structure
├── data/
│   └── marketing_campaign.csv
├── sql/
│   └── segmentation_queries.sql
├── excel/
│   └── analysis_dashboard.xlsx
├── images/
│   └── (charts & graphs)
└── README.md
