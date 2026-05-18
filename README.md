# Customer Segmentation to Reduce Marketing Wastage

## SQL + Excel Consumer Insight Case Study

This project uses the Kaggle **Customer Personality Analysis** dataset to build customer personas and recommend more efficient campaign targeting.

> **Business Question:**  
> How can customer segmentation reduce ad wastage and improve campaign ROI by identifying who to target, where to target them, and what offer to use?

This is a portfolio-ready case study for **Market Analyst**, **Consumer Insight Analyst**, and **Consumer Behavior Analyst** roles.

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/7a536b1b1a169197d3d4138751c870d8a66abb96/project_workflow.svg)

---

## Executive Summary

Three customer personas were identified:

| Persona | Customer Count | Avg Spend | Campaign Response | Channel Signal | Discount Sensitivity | Decision |
|--------|---------------:|----------:|------------------:|--------------|---------------------:|----------|
| **Premium Omnichannel Buyers** | 925 | 1193.46 | 42.5% | Store + Catalog | 11.2% | Prioritize |
| **Deal-Driven Digital Browsers** | 435 | 358.05 | 32.4% | Web | 37.7% | Selective |
| **Low-Engagement Occasional Buyers** | 853 | 98.05 | 8.2% | Low activity | 32.7% | Suppress |

**Final Recommendation:**
- Prioritize **Premium Omnichannel Buyers**
- Selectively target **Deal-Driven Digital Browsers**
- Reduce spend on **Low-Engagement Occasional Buyers**

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/7cb2901f40fb40492f0cd7f1ea84700a435b7ff7/persona_cards.svg)

---

## Dataset

- **Source:** Kaggle Customer Personality Analysis  
- **Link:** https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis  

### Dataset Size

| Item | Count |
|------|------:|
| Raw customers | 2,240 |
| Missing income | 24 |
| Final dataset | 2,213 |
| Variables | 29 |

---

## Tools Used

- **SQL / SQLite** → data cleaning & segmentation  
- **Excel** → dashboard & charts  
- **Markdown + SVG** → GitHub documentation  

---

## Methodology

### 1. Data Cleaning
- Removed missing income records  
- Removed unrealistic age outliers  
- Dropped non-informative columns  

### 2. Feature Engineering

Key metrics:
- `Total_Spend`
- `Total_Purchases`
- `Deal_Share`
- `Web_Share`, `Store_Share`, `Catalog_Share`
- `Campaign_Response`

### 3. Persona Logic

| Persona | Description |
|--------|------------|
| Premium Omnichannel | High value + high engagement |
| Deal-Driven Digital | Discount-sensitive + web-focused |
| Low-Engagement | Low value + low response |

---

## Persona Insights

### Spend Comparison

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/25d51861063b97aabd2584cb90a04b82072f3f34/avg_spend_by_persona.svg)

**Insight:**  
Premium customers spend **3–12x more** than other groups.

---

### Product Preferences

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/25d51861063b97aabd2584cb90a04b82072f3f34/product_spend_by_persona.svg)

**Insight:**  
Premium buyers dominate across all categories → ideal for **bundling & upselling**

---

### Campaign Response

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/25d51861063b97aabd2584cb90a04b82072f3f34/campaign_response_by_persona.svg)

**Insight:**
- Premium = strongest response  
- Digital = responsive but price-sensitive  
- Low-engagement = poor ROI  

---

### Channel Behavior

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/0e272ad36a60892844232509c759e1d29815431b/channel_preference_by_persona.svg)

| Persona | Strongest Channel |
|--------|------------------|
| Premium | Store |
| Digital | Web |
| Low-engagement | Store |

---

### Discount Sensitivity

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/0e272ad36a60892844232509c759e1d29815431b/discount_sensitivity_by_persona.svg)

**Insight:**  
Digital users rely heavily on discounts → margin risk.

---

## ROI Proxy

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/bb38f50b45f6e13ad15ac5f81a30b140202c60e6/response_value_index.svg)


---

## Final Targeting Mix

![image alt](https://github.com/MustafaKhalid04/Customer-Segmentation-to-Reduce-Marketing-Wastage/blob/bb38f50b45f6e13ad15ac5f81a30b140202c60e6/targeting_matrix.svg)
