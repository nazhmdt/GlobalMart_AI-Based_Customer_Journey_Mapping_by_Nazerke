# 🛍️ GlobalMart AI-Based Customer Journey Mapping

> End-to-end AI marketing analytics project for a fictional multinational retailer — from customer journey mapping to CLV, churn prediction, RFM segmentation, sentiment analysis, recommendations, attribution modeling, CRO, and Power BI export.

---

## 📌 Overview

This project focuses on **AI-based customer journey mapping** for GlobalMart, a fictional multinational retail chain operating across five regions:

- Central Asia
- Europe
- MENA
- North America
- Southeast Asia

The goal is to understand how customers move through the marketing journey, identify high-value and high-risk customers, predict churn, analyze customer sentiment, build recommendation logic, evaluate marketing channels, and prepare business-ready outputs for Power BI.

The project combines statistical methods, machine learning, NLP, recommendation systems, attribution modeling, and customer analytics.

---

## 📂 Project Structure

```text
globalmart-ai-journey/
├── customers.csv                         # Customer profiles and demographics
├── transactions.csv                      # Transaction and purchase history
├── touchpoints.csv                       # Customer journey touchpoint data
├── reviews.csv                           # Customer review text and sentiment data
├── churn_labels.csv                      # Customer churn labels
├── GlobalMart_AI_Journey_.ipynb          # Full AI customer journey analytics pipeline
├── powerbi_region_summary.csv            # Exported regional summary for Power BI
├── powerbi_rfm_customers.csv             # Exported RFM customer-level data
├── powerbi_monthly_transactions.csv      # Exported monthly transaction data
└── README.md
``` 

---

## 🔍 Analysis Pipeline

**1. Data Loading & Inspection** — loaded five datasets, checked shapes, columns, and customer structure

Datasets used:

- `customers.csv`
- `transactions.csv`
- `touchpoints.csv`
- `reviews.csv`
- `churn_labels.csv`

Dataset sizes:

- Customers: **5,000 rows**
- Transactions: **58,276 rows**
- Touchpoints: **40,312 rows**
- Reviews: **3,000 rows**
- Churn Labels: **5,000 rows**

**2. Markov Chain Journey Modeling**
- Built a customer journey transition matrix
- Analyzed movement between stages:
  - Awareness
  - Consideration
  - Purchase
  - Retention
  - Advocacy
- Calculated long-run stage probabilities
- Measured probability of customers moving from Consideration to Purchase

**3. Customer Lifetime Value Calculation**
- Calculated CLV using discounted future value logic
- Compared customer value by region and segment
- Identified top CLV customers
- Measured total portfolio CLV

**4. Churn Prediction**
- Built a Logistic Regression churn prediction model
- Used customer behavior, transaction, and engagement features
- Evaluated model using classification report and ROC AUC
- Identified high-risk customers by region

**5. RFM Scoring and Neural Network Model**
- Calculated Recency, Frequency, and Monetary values
- Created RFM customer segments
- Trained a neural network model for churn prediction
- Compared churn prediction performance with machine learning methods

**6. Sentiment Analysis and NLP**
- Analyzed customer review sentiment
- Compared lexicon-based sentiment with ground truth labels
- Built TF-IDF + Naive Bayes sentiment classifier
- Evaluated sentiment classification performance

**7. Recommendation System**
- Built a user-item matrix by customer and product category
- Calculated product category similarity
- Generated personalized category recommendations
- Used collaborative filtering logic to recommend next product categories

**8. Attribution Modeling**
- Compared multiple marketing attribution models:
  - First Touch
  - Last Touch
  - Linear Attribution
  - Time Decay
  - Position-Based Attribution
- Evaluated channel contribution to conversions
- Compared Online, Mobile App, In-Store, and Call Center channels

**9. Conversion Rate Optimization**
- Calculated conversion rates by channel and campaign
- Compared campaign performance
- Ran A/B test between Loyalty Push and Black Friday campaigns
- Used chi-square test to check statistical significance

**10. Power BI Export**
- Created final exports for dashboard development:
  - `powerbi_region_summary.csv`
  - `powerbi_rfm_customers.csv`
  - `powerbi_monthly_transactions.csv`

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C9ED9?style=flat)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![NLTK](https://img.shields.io/badge/NLTK-154F3C?style=flat)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)

---

## 💡 Key Findings

- Customers in the **Consideration** stage move to **Purchase** with a probability of about **20.1%**.
- Long-run journey distribution shows that most customers remain in **Consideration** and **Awareness** stages.
- Total portfolio CLV reached approximately **$28.7M**.
- The Logistic Regression churn model achieved very strong performance with **ROC AUC = 1.0000**.
- The Neural Network churn model also showed strong performance with **ROC AUC = 0.9998**.
- RFM segmentation identified several meaningful customer groups, including Champions, Loyal Customers, Potential Loyalists, At Risk, Recent Customers, and Lost customers.
- Lexicon-based sentiment analysis achieved **96.87% accuracy**.
- TF-IDF + Naive Bayes sentiment classifier achieved almost perfect classification results.
- Online and Mobile App channels received the highest attribution credit across most attribution models.
- The A/B test between Loyalty Push and Black Friday was **not statistically significant** at α = 0.05.

---

## 🔗 Customer Journey Insights

The Markov Chain model was used to understand how customers move between journey stages.

| Journey Stage | Long-Run Probability |
|---|---:|
| Awareness | 25.02% |
| Consideration | 30.01% |
| Purchase | 20.10% |
| Retention | 14.91% |
| Advocacy | 9.96% |

The probability of moving from **Consideration** to **Purchase** was approximately **20.1%**.

This means that only around one in five customers who consider the brand actually move to the purchase stage.

---

## 💰 CLV Insights

Customer Lifetime Value was calculated to estimate the long-term financial value of each customer.

| Metric | Value |
|---|---:|
| Average CLV | $5,740.30 |
| Median CLV | $2,903.42 |
| Maximum CLV | $43,613.02 |
| Total Portfolio CLV | $28,701,511 |

Top CLV customers mainly belonged to the **Premium** segment and came from regions such as Europe, MENA, and North America.

---

## ⚠️ Churn Prediction

The churn prediction model used customer behavior and engagement features such as:

- recency
- frequency
- monetary value
- average order value
- number of channels
- number of categories
- return rate
- payment delay
- discount usage
- support contacts
- app sessions
- age
- region
- segment

### Logistic Regression Performance

| Metric | Result |
|---|---:|
| Accuracy | 0.99 |
| ROC AUC | 1.0000 |

High-risk customer count by region:

| Region | High-Risk Customers |
|---|---:|
| North America | 328 |
| Europe | 302 |
| MENA | 210 |
| Southeast Asia | 185 |
| Central Asia | 139 |

---

## 🧠 RFM Segmentation

RFM scoring was used to segment customers based on:

- **Recency** — how recently the customer purchased
- **Frequency** — how often the customer purchased
- **Monetary** — how much the customer spent

| Segment | Customer Count |
|---|---:|
| Potential Loyalists | 1,966 |
| Champions | 1,125 |
| Loyal Customers | 648 |
| Lost | 584 |
| Recent Customers | 374 |
| At Risk | 303 |

These segments can help the business create different marketing strategies for different customer groups.

---

## 💬 Sentiment Analysis

Customer reviews were analyzed using two approaches:

| Method | Result |
|---|---:|
| Lexicon-Based Sentiment | 96.87% accuracy |
| TF-IDF + Naive Bayes | 1.00 accuracy |

The sentiment analysis helped classify customer reviews into:

- Positive
- Neutral
- Negative

This can help GlobalMart understand customer satisfaction and detect potential service issues.

---

## 🎯 Recommendation System

A recommendation system was created using customer-category purchase behavior.

The project built:

- user-item matrix
- category similarity matrix
- personalized category recommendations

The recommendation system can help suggest the next best product categories for each customer based on previous purchase patterns.

Example business use:

- recommend Beauty products to customers who buy Fashion and Electronics
- recommend Sports products to customers with similar purchase behavior
- personalize offers by customer profile and product category

---

## 📡 Attribution Modeling

The project compared different attribution models to understand channel contribution.

Channels analyzed:

- Online
- Mobile App
- In-Store
- Call Center

| Channel | First Touch | Last Touch | Linear | Time Decay | Position-Based |
|---|---:|---:|---:|---:|---:|
| Online | 37.1% | 37.1% | 38.2% | 38.0% | 37.4% |
| Mobile App | 30.4% | 31.6% | 30.2% | 30.5% | 30.7% |
| In-Store | 26.8% | 26.4% | 26.5% | 26.5% | 26.6% |
| Call Center | 5.8% | 4.9% | 5.1% | 5.0% | 5.3% |

Online and Mobile App channels contributed the most to customer conversions.

---

## 📈 Conversion Rate Optimization

Conversion rate was calculated by channel.

| Channel | Visits | Conversions | Conversion Rate |
|---|---:|---:|---:|
| Call Center | 2,028 | 244 | 12.03% |
| In-Store | 10,687 | 1,232 | 11.53% |
| Mobile App | 12,164 | 1,400 | 11.51% |
| Online | 15,433 | 1,680 | 10.89% |

The A/B test compared **Loyalty Push** and **Black Friday** campaigns.

| Campaign | Conversion Rate |
|---|---:|
| Loyalty Push | 10.93% |
| Black Friday | 11.74% |

A/B test result:

```text
p-value = 0.1389
Result: Not Significant at α = 0.05
```

This means the difference between the two campaigns was not statistically significant.

---

## 🌍 Regional Executive Summary

| Region | Customers | Total Revenue | Avg CLV | Churn Rate | Positive Sentiment | Conversion Rate |
|---|---:|---:|---:|---:|---:|---:|
| MENA | 877 | $8,134,811 | $5,753 | 23.8% | 73.1% | 11.14% |
| Southeast Asia | 730 | $6,642,936 | $5,646 | 24.8% | 67.7% | 10.92% |
| North America | 1,522 | $14,508,601 | $5,940 | 20.9% | 72.1% | 11.34% |
| Europe | 1,243 | $10,987,450 | $5,541 | 23.5% | 71.1% | 11.63% |
| Central Asia | 628 | $5,776,251 | $5,742 | 22.0% | 69.5% | 11.24% |

---

## 📊 Power BI Dashboard

The project exports final datasets for Power BI dashboard creation.

Power BI pages can include:

- Executive Overview
- Regional Performance
- Customer Journey Funnel
- CLV Analysis
- Churn Risk Analysis
- RFM Segmentation
- Sentiment Insights
- Channel Attribution
- Conversion Rate Optimization

Exported files:

```text
powerbi_region_summary.csv
powerbi_rfm_customers.csv
powerbi_monthly_transactions.csv
```

---

## 📌 Business Recommendations

### 1. Improve conversion from Consideration to Purchase

Only about 20.1% of customers move from Consideration to Purchase.

Recommended actions:
- improve product comparison pages
- create personalized offers
- use retargeting campaigns
- reduce checkout friction
- test stronger call-to-action messages

---

### 2. Focus retention campaigns on high-risk regions

North America and Europe have the largest number of high-risk customers.

Recommended actions:
- launch churn prevention campaigns
- prioritize high-CLV customers
- offer loyalty incentives
- monitor customers with high support contacts and payment delays

---

### 3. Use RFM segments for campaign personalization

Different customer segments need different marketing strategies.

Recommended actions:
- reward Champions
- nurture Potential Loyalists
- reactivate At Risk customers
- win back Lost customers
- onboard Recent Customers with personalized offers

---

### 4. Strengthen Online and Mobile App channels

Online and Mobile App channels generate the highest attribution credit.

Recommended actions:
- invest more in digital customer experience
- improve app engagement
- personalize online recommendations
- use digital channels for retention and cross-selling

---

### 5. Use sentiment analysis for customer experience improvement

Review sentiment can help detect satisfaction problems earlier.

Recommended actions:
- monitor negative reviews
- identify repeated complaints
- connect sentiment with churn risk
- improve service quality based on review patterns

---

## 📌 Business Value

This project shows how AI and analytics can improve marketing decision-making across the full customer journey.

The results can help GlobalMart:

- understand customer journey transitions
- identify high-value customers
- predict churn risk
- create customer segments
- analyze customer sentiment
- recommend products and categories
- evaluate marketing channels
- improve conversion rates
- prepare Power BI dashboards for business users
- support data-driven marketing strategy

---

## 👥 Team

**Nazerke Zhumadilova** · [@nazhmdt](https://github.com/nazhmdt)  
**Inzhu Nurlan** · [@InzhuNurlan](https://github.com/InzhuNurlan)

---

## 🎓 Course

**AI in Marketing** — Astana IT University  
Professor: **Muhammed Ali Ibrahim**
