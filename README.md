# 1. EXECUTIVE SUMMARY

Rainbow Retail, a global eCommerce start-up specialising in technology products, has undergone significant revenue fluctuations from 2019 to 2022. While 2020 marked a period of rapid growth (+163% revenue increase), the subsequent years saw declines in both revenue (-46%) and order count (-40%), highlighting shifting consumer behaviour and potential operational inefficiencies. This analysis evaluates key performance trends, customer purchasing behaviour and marketing effectiveness to identify strategic opportunities for sustainable growth.

## Key Findings:
- **Revenue & Growth**: 2020's surge was driven by high order volume and AOV but declined post-pandemic due to reduced demand for premium products.
- **Market Performance**: North America remains the strongest market, whereas Latin America underperforms across all metrics, suggesting potential for regional expansion.
- **Product Trends**: High-value items like MacBook Air and ThinkPad laptops contributed to a higher AOV, but declines in these categories negatively impacted overall revenue.
- **Marketing Effectiveness**: Direct marketing remains the most effective channel, while social media strategies require optimisation to drive better engagement and conversions.

## Actionable Recommendations:
- **Stabilise Growth**: Implement customer retention strategies like loyalty-based incentives and personalised promotions.
- **Enhance Consumer Experience**: Optimise checkout processes and introduce multiple payment options to increase conversions.
- **Strengthen Affiliate Partnerships**: Expand influencer marketing and exclusive discount codes to boost high-value sales.
- **Expand into Latin America**: Adapt successful North American strategies for better market penetration.
- **Optimise Social Media Marketing**: Run A/B tests on content and targeting to improve conversion rates.

By addressing these areas, Rainbow Retail can achieve sustainable revenue growth, better market positioning and improved customer retention.

---

# 2. OVERVIEW

Rainbow Retail is an eCommerce start-up selling mostly technology devices to various regions of the world. After four years of operations, the company has decided to have a closer look at the data collected since its inception in 2019. Of particular importance to the sales executives are questions related to revenue and growth. The objective of this analysis is to evaluate sales performance trends, customer purchasing behaviour and marketing effectiveness for Rainbow Retail. By examining key metrics—revenue, order count and average order value (AOV)—the goal is to identify areas for growth, optimisation and strategic decision-making.

## To provide actionable insights, this analysis seeks to answer the following questions:
- What are the overall trends in sales performance?
- What are the key drivers of revenue and AOV?
- How is customer behaviour changing, and how should the business respond?
- Which regions and marketing channels are most effective?

## This analysis covers four key areas:
- **Sales Trends**: Year-over-year analysis of revenue, order count and AOV to track growth and decline.
- **Customer Segments**: Breakdown of loyalty vs. non-loyalty customers and their contribution to revenue.
- **Product Performance**: Identification of top-selling and underperforming products.
- **Marketing & Regional Insights**: Evaluation of marketing channel effectiveness and regional sales performance.

---

# 3. DATA OVERVIEW

Each record in the table represents a single transaction or order placed by a customer. The columns contain details about the transaction, the customer, the product, and other relevant data points. Here's a breakdown of each field:
- **user_id**: Unique identifier for each customer.
- **order_id**: Unique identifier for each purchase transaction.
- **purchase_ts**: Timestamp when the order was placed.
- **purchase_day**: Day of the week when the order was placed.
- **purchase_month**: Month when the order was placed.
- **purchase_year**: Year when the order was placed.
- **ship_ts**: Date when the order was shipped.
- **delivery_ts**: Date when the order was delivered.
- **refund_ts**: Date when the order was refunded (if applicable).
- **is_refund**: Indicates whether the order was refunded (1 = Yes, 0 = No).
- **product_name**: Name of the purchased product.
- **product_id**: Unique identifier for the purchased product.
- **usd_price**: Price of the product in USD.
- **local_price**: Price of the product in the local currency.
- **currency**: Currency used for the purchase.
- **purchase_platform**: Platform where the purchase was made (e.g., Website, Mobile App).
- **marketing_channel**: Channel that drove the purchase (e.g., Direct, Social Media, Affiliate).
- **account_creation_method**: How the customer created their account (e.g., Desktop, Mobile).
- **country_code**: Two-letter country code representing the customer's location.
- **loyalty_programme**: Indicates whether the customer is part of a loyalty programme (1 = Yes, 0 = No).
- **created_on**: Date when the customer's account was created.
- **created_on_check**: Verification flag for account creation consistency (TRUE/FALSE).

---

# 4. KEY INSIGHTS

### a. Metrics:
- **Sales**: The total monetary value of all completed transactions within a given period.
- **Revenue**: The total income generated from sales before deducting expenses.
- **Order Count**: The total number of individual purchase transactions made by customers.
- **Average Order Value (AOV)**: The average amount spent per order, calculated as the average of revenue.

### b. Revenue Trends:
- 2020 saw a major increase in revenue (+163%) compared to 2019 but revenue declined (-46%) from 2021 to 2022.
- In 2022, revenue is currently at R5M.
- **Top revenue-generated products**:
  - 27in 4K Gaming Monitor, Apple AirPods Headphones and MacBook Air Laptop accounted for R24M (85%) of total revenue.
- **Worst-performing product by revenue**:
  - Bose Soundsport Headphones had the lowest revenue.
  - Apple iPhone had the second-lowest revenue.
- **Regional breakdown**:
  - North America led with R14.5M in revenue.
  - Latin America had the lowest revenue.
- **Marketing channel impact**:
  - Direct marketing generated R23M (83%) of total revenue.

### c. Order Count Trends:
- Order volume surged by 101% in 2020 but dropped (-40%) from 2021 to 2022.
- In 2022, total orders stand at 21K.
- **Top-selling product**:
  - Apple AirPods Headphones had the highest order count (48K).
- **Worst-performing product by order count**:
  - Bose Soundsport Headphones.
- **Regional order volume**:
  - North America led with 55K orders.
  - Latin America had the lowest order count.
- **Customer segment performance**:
  - Non-loyalty customers placed more orders than loyalty customers.
- **Marketing channel impact**:
  - Direct marketing drove 84K orders.

### d. Average Order Value (AOV) Trends:
- AOV increased by 31% in 2020 but declined by 10% in 2022, settling at R230.
- **Highest AOV products**:
  - MacBook Air Laptop (R1.5K per order).
  - ThinkPad Laptop (R1.1K per order).
  - Apple iPhone had a below-average order count but a relatively high AOV (R741).
- **Regional AOV trends**:
  - Asia Pacific had the highest AOV (R279 per order).
- **Marketing channels & AOV**:
  - Affiliates generated the highest-value purchases, with an AOV of R303.

---

# 5. DETAILED ANALYSIS

### a. Revenue Trends: Growth and Decline
- **2020 Revenue Surge (+163%)** primarily driven by:
  - A 101% increase in order count, showing more customers were making purchases.
  - A 31% rise in AOV, indicating customers were spending more per order.
  - Strong sales of high-ticket products such as the MacBook Air Laptop and 27in 4K Gaming Monitor.
  - Direct marketing efforts, which contributed R23M (83%) of total revenue.
- **2021-2022 Revenue Decline (-46%)**:
  - A 40% decline in order count, suggesting fewer customers were purchasing.
  - A 10% drop in AOV, meaning customers spent less per transaction.
  - A possible shift in consumer spending habits post-pandemic, impacting demand for premium electronics.
  - Poor performance of certain product categories, like the Bose Soundsport Headphones and Apple iPhone.
  - Weak revenue generation in Latin America.

### b. Order Count: Consumer Demand and Shopping Behaviour
- **2020 Order Boom (+101%)**:
  - A major increase in consumer demand and eCommerce growth likely contributed to a high volume of orders.
  - Direct marketing campaigns played a significant role, driving 84K orders.
  - Apple AirPods Headphones were the most purchased item, with 48K orders.
- **2021-2022 Order Decline (-40%)**:
  - A reduction in total orders suggests a decline in demand or a shift in consumer preferences.
  - Non-loyalty customers placed more orders than loyalty customers, indicating that acquiring new customers played a key role in driving sales.

### c. AOV: Spending Behaviour and High-Value Purchases
- **2020 AOV Growth (31%)**:
  - The increase in high-ticket purchases such as MacBook Air (R1.5K AOV) and ThinkPad (R1.1K AOV) laptops drove the rise in AOV.
- **2021-2022 AOV Decline (-10%)**:
  - A drop in premium product sales or a shift to lower-cost items contributed to the decline.

### d. Regional Performance: Market Strengths and Weaknesses
- **North America (Strongest Region)**:
  - Led in revenue (R14.5M), order count (55K), and customer base (45K).
- **Asia Pacific (High AOV, Moderate Order Count)**:
  - Highest AOV (R279 per order), indicating that customers in this region tend to make larger purchases.
- **Latin America (Weakest Performance)**:
  - Performed the worst across all metrics.

### e. Marketing Channel Performance: What Is Driving Sales
- **Direct Marketing**:
  - Generated R23M (83%) of total revenue and 84K orders.
- **Affiliate Marketing**:
  - AOV was the highest at R303 per order, but order volume was lower than direct marketing.
- **Social Media & Unknown Channels**:
  - Both performed poorly across all metrics, signalling a need for better targeting and engagement.

---

# 6. ACTIONABLE RECOMMENDATIONS

- **Stabilise Long-Term Growth**:
  - Implement loyalty-based incentives such as discounts, early access or personalised offers.
- **Shifting Consumer Behaviour**:
  - Optimise the checkout process to reduce friction and increase conversion rates.
- **Strengthen Affiliate Marketing Relationships**:
  - Develop exclusive discount codes for influencers to increase reach.
- **Expansion Opportunity**:
  - Identify key success factors in North America and adapt them to Latin America.
- **Ad Optimisation**:
  - A/B test social media content for better conversion rates.
