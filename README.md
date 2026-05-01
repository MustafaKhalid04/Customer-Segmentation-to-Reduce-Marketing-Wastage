📊 Customer Segmentation to Reduce Marketing Wastage

--
🔍 Project Overview
This project uses the Customer Personality Analysis dataset from Kaggle to build actionable customer personas and optimize marketing strategy.

--
Business Objective:
Identify who to target, where to target them, and what offer to use in order to reduce marketing wastage and improve campaign ROI.

--
This project is designed for roles such as:
Market Analyst
Consumer Insight Analyst
Consumer Behavior Analyst
It combines segmentation, campaign response analysis, channel preference analysis, and discount sensitivity analysis using SQL and Excel.
📁 Dataset
Source: Kaggle – Customer Personality Analysis
File location: data/marketing_campaign.csv
Note: File is tab-separated (.tsv format) despite .csv extension
❓ Business Questions
Which customer personas are most valuable?
Which personas waste marketing budget?
Which channel works best for each persona?
Which customers are discount-sensitive?
What campaign strategy maximizes ROI?
👥 Persona Framework
Customers are grouped into 3 business-friendly personas using a transparent scoring model:
Persona	Core Behavior	Targeting Role
Premium Omnichannel Buyers	High spend, high activity, multi-channel	🎯 Highest priority
Deal-Driven Digital Browsers	High web + discount usage	⚖️ Selective targeting
Low-Engagement Occasional Buyers	Low spend, low response	🚫 Suppress
⚙️ Methodology
1. Segmentation Analysis
Key features used:
Total spend & category spend
Web, store, catalog purchases
Web visits
Deal purchases
Recency
Campaign responses
📊 Add chart here:
![Customer Segmentation](images/segmentation_chart.png)
2. Campaign Response Analysis
Metrics:
AcceptedCmp1–AcceptedCmp5
Overall response rate
Total accepted campaigns
📊 Add chart here:
![Campaign Response by Persona](images/campaign_response.png)
3. Channel Preference Analysis
Comparison across:
Web
Store
Catalog
⚠️ Note: Used as efficiency proxy, not true ROI (no cost data available)
📊 Add chart here:
![Channel Preference](images/channel_analysis.png)
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
🎯 Recommended Campaign Strategy
Persona	Who to Target	Channel	Offer Strategy	ROI View
Premium Omnichannel Buyers	First priority	Catalog, Store, Email	Loyalty rewards, premium bundles	⭐ Best ROI
Deal-Driven Digital Browsers	Secondary	Web, Email	Limited-time discounts	⚖️ Medium ROI
Low-Engagement Buyers	Avoid	Low-cost email only	Win-back offers	🚫 High wastage
🛠 Tools Used
SQL (segmentation & aggregation)
Excel (analysis & visualization)
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
