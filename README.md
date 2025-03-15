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

The company's main database structure, as seen below, consists of four tables: orders, customers, geo_lookup and order_status. A description of each table is as follows:

- **orders** - stores information related to individual customer purchases. It currently contains 108127 records.
- **customers** - holds customer details. 
- **geo_lookup** - maps country codes to specific regions, providing geographical context for customer orders. 
- **order_status** - tracks the status of each order. 

<p align="center">
  <img src="https://github.com/user-attachments/assets/84174577-dafc-4850-820e-cdc93ff0e25f" />
</p>


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
  - Affiliates attracted high-value purchases with an AOV of R303, suggesting that partnerships played a role in driving larger transactions
  - Asia Pacific led in AOV (R279 per order), indicating that regional pricing strategies or consumer preferences in this market favoured larger purchases
- **AOV by Product**:
  - MacBook Air and ThinkPad Laptops produced the highest AOV (R1.5K and R1.1K, respectively)
  - Apple iPhone had one of the lowest Order Counts but a relatively strong AOV (R741), suggesting that while fewer customers purchased iPhones, those who did spent more


### d. Regional Performance: Market Strengths and Weaknesses
- **North America (Strongest Region)**:
  - Led in revenue (R14.5M), order count (55K), and customer base (45K).
  - Suggests strong brand presence, effective marketing and high consumer trust in the region.
- **Asia Pacific (High AOV, Moderate Order Count)**:
  - Highest AOV (R279 per order), indicating that customers in this region tend to make larger purchases.
  - Order Count was not as strong as North America which may suggest a need for better marketing penetration
- **Latin America (Weakest Performance)**:
  - Performed the worst across all metrics.
  - Possible reasons include lower market penetration, weaker brand recognition or economic factors affecting consumer spending.

### e. Marketing Channel Performance: What Is Driving Sales
- **Direct Marketing (Top Performer)**:
  - Generated R23M (83%) of total revenue and 84K orders.
  - This suggests targeted campaigns and direct outreach strategies were highly effective in converting customers.
- **Affiliate Marketing (High AOV but Lower Volume)**:
  - AOV was the highest at R303 per order but order volume was lower than Direct marketing.
  - However, Order volume was not as high as direct marketing, meaning there could be an opportunity to expand affiliate partnerships to drive more order.
- **Social Media & Unknown Channels (Poor Performers)**:
  - •	Both performed poorly across all metrics, signalling that these channels ay need improved targeting, better engagement strategies or increased budget allocation to be more effective.

### f. Key Takeaways
- The business experienced a strong surge in 2020 but faced a decline in 2021-2021, indicating the need to stabilise long-term growth
- Revenue and Order Count declines suggest shifting consumer behaviour, requiring improved marketing efforts to retain and attract customers
- High-value product sales (MacBook Air and ThinkPad) and premium purchases through affiliates drove AOV but a decline in these areas contributed to lower overall Revenue
- North America is the strongest market, while Latin America is the weakest, indicating an opportunity for targeted expansion
- Direct marketing is the most effective channel, while social media strategies need improvement.

---

# 6. ACTIONABLE RECOMMENDATIONS

- **Stabilise Long-Term Growth**:
  - Strategy team to implement loyalty-based incentives such as discounts, early access or personalised offers to encourage repeat purchases.
- **Shifting Consumer Behaviour**:
  - CX team to optimise the checkout process to reduce friction and increase conversion rates (e.g. multiple payment options, guest checkout).
- **Strengthen Affiliate Marketing Relationships**:
  - Marketing team to develop exclusive discount codes for influencers to increase reach.
- **Expansion Opportunity**:
  - Sales team to identify key success factors in North America (e.g. top-selling products, marketing channels) and adapt them to Latin America.
- **Ad Optimisation**:
  - •	Data analytics team to A/B test social media content for better conversion rates.
