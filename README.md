# RAINBOW RETAIL
# Data Analysis Report: Sales Performance 2018-2022

| **Section**                            | **Details**                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Executive Summary**                  | This report evaluates Rainbow Retail's sales performance from 2018 to 2022. <br>The analysis, based on synthetic data, highlights key trends and offers actionable insights to optimise future business strategies.<br> Rainbow Retail has demonstrated consistent growth in sales and revenue from 2018 to 2022, with echnology products leading the market share. This growth occurred against a backdrop of significant local and global economic events that likely influenced consumer behavior and market trends. <br>Strategic recommendations are provided to enhance product portfolio, marketing strategies and regional sales efforts, aligned with broader business goals such as market expansion, product diversification and customer retention.   |
| **Introduction**                       | Rainbow Retail, a South African e-commerce retailer specialising in office supplies, furniture and technology products, aims to leverage data insights to refine its sales strategy and improve market position. <br>This report outlines the current sales performance and identifies strategic opportunities for growth and optimisation.       |
| **Economic Context** | 1. *COVID-19 Pandemic (2020-2022)*: <br>- Global lockdowns led to increased online shopping. <br>- Supply chain disruptions affected product availability and shipping costs. <br>- Economic uncertainty influenced consumer spending patterns.  <br><br>2. *South African Economic Challenges*: <br>- Slow economic growth and high unemployment rates. <br>- Load shedding affecting business operations. <br>- Currency fluctuations impacting import costs. <br><br>3. *Global Tech Trends*: <br>- Rapid advancements in technology driving demand for new products. <br>- Shift towards remote work and learning boosting sales of tech products. <br><br>4. *E-commerce Boom*: <br>- Accelerated adoption of online shopping due to the pandemic. <br>- Increased competition in the e-commerce space. <br><br>5. *Global Supply Chain Issues*: <br>- Shortages of semiconductors and other components affecting tech product availability. <br>- Increased shipping costs and delays impacting furniture and other bulky items.|
| **Data Overview**                      | <br> ![image](https://github.com/user-attachments/assets/fa16c65d-3c4c-45ae-8825-9c9e83d1a69f) <br>The analysis uses synthetic data representing customers, sales, products and temporal entities, allowing for comprehensive tracking of sales transactions and trends. The data spans from January 2018 to December 2022. |
| **Analysis**                           | **Sales and Revenue Growth Trend** <br> ![image](https://github.com/user-attachments/assets/a2602ec4-155c-474c-acc3-6281749b2dc4)<br> *Insight*: A general upward trajectory in monthly sales and revenue indicates robust growth. Rainbow Retail's ability to maintain growth is noteworthy given the economic turbulence. This suggests the company successfully adapted to changing market conditions and consumer behaviors. <br><br> *Strategic Goal*: Market Expansion. Capitalise on the growth trend by exploring new market segments and expanding product lines to maintain momentum. <br><br> **Product Category Performance** <br> ![image](https://github.com/user-attachments/assets/857be2af-3744-44ae-aa96-abde1bb6c8ca) <br> *Insight*: Technology products dominate with 49% of total revenue, while the furniture category underperforms at 3%. The strong performance of technology products aligns with global trends accelerated by the pandemic. Remote work and online learning likely boosted demand for computers, tablets and related accessories. Rainbow Retail's ability to meet this demand despite supply chain challenges suggests effective inventory management. The low contribution of furniture may be attributed to: <br>- Higher shipping costs and logistical challenges during the pandemic, <br>- Consumer hesitancy to make large purchases online, especially during economic uncertainty. <br>- Potential supply issues due to global manufacturing and shipping disruptions. <br><br> *Strategic Goal*: Product Diversification. Expand the range of technology products and enhance the promotion of underperforming categories like furniture to reduce dependency on a few product lines. <br><br>  **Top-Selling Products** <br> ![image](https://github.com/user-attachments/assets/a5782f1e-b551-4d9c-a2ee-c32248c977ef) <br> *Insight*: A few key products, like the High-Speed Automatic Electric Letter Opener, drive significant sales. <br><br>*Strategic Goal*: Revenue Maximisation. Develop upselling and cross-selling strategies around these top-performing products to boost the Average Order Value (AOV) and overall revenue. <br><br>  **Sales by Province** <br> ![image](https://github.com/user-attachments/assets/08e15f7e-691e-454f-bf22-5d620fd5d6f8) <br> *Insight*: KwaZulu-Natal, Gauteng and Eastern Cape are leading markets, with potential growth opportunities in Limpopo and Northern Cape. Concentration in Gauteng, Western Cape and KwaZulu-Natal reflects the economic importance of these provinces. Lower sales in other regions may indicate: <br>- Economic disparities across provinces. <br>- Varying levels of internet penetration and e-commerce adoption. <br>- Potential for targeted growth strategies in underserved areas.<br><br>*Strategic Goal*: Geographical Expansion. Focus marketing efforts on underperforming regions to balance sales distribution and enhance overall market penetration. <br><br>  **Average Order Value (AOV)** <br> *Insight*: The AOV stands at R4,467, providing insights into purchasing behavior. Higher AOVs for technology and furniture align with the typically higher prices of these items. Regional AOV differences may reflect: <br>- Varying economic conditions across provinces. <br>- Different product preferences or availability in certain areas.<br><br>*Strategic Goal*: Customer Retention and Value Enhancement. Implement targeted marketing campaigns and "smart shopper" programmes to encourage higher spending and repeat purchases.|  
| **Recommendations**                    | **Product Portfolio Optimisation** <br> - Expand the technology product line and consider strategic partnerships to boost the furniture category. <br> - Investigate unclassified products to identify emerging market trends and opportunities for new product categories.<br><br> **Sales and Marketing Strategy Enhancement** <br> - Intensify marketing efforts in high-performing regions and develop targeted campaigns in regions with growth potential. <br>- Use insights from AOV analysis to tailor product bundles and promotional offers. <br> - Investigate barriers to growth in underperforming regions and develop strategies to address them. <br><br>**Data Analysis and Reporting Enhancement** <br> - Improve data categorisation to ensure accurate reporting and deeper customer behavior analysis, assisting in more informed strategic decisions. <br>- Develop predictive models that incorporate economic indicators to anticipate market trends.|
| **Assumptions**                        | Data completeness issues, such as the significant portion of revenue from unclassified categories, may impact the accuracy of the analysis.                                                                                                                                                           |
| **Technical Approach**                 | The analysis utilised advanced Excel features such as Power Query and Power Pivot and SQL for data extraction, transformation and loading. This approach facilitated comprehensive data analysis and insightful reporting.                                                                                                                                                                                     |
| **Conclusion**                         | By implementing these strategic recommendations, Rainbow Retail can enhance its sales performance, optimise product offerings and strengthen its market presence. Aligning data insights with strategic business goals will ensure sustained growth and competitive advantage in the South African e-commerce market.                                                                                                        |

<br> **Ad-Hoc Queries** <br> Common questions translated into technical SQL queries.  

```sql
-- Query 1: Top Products by Total Sales Amount

WITH ProductSales AS (
    SELECT p.product_name, SUM(s.sales) AS total_sales
    FROM sales s
    JOIN Products p ON s.product_id = p.product_id
    GROUP BY p.product_name
)
SELECT product_name, total_sales,
       RANK() OVER (ORDER BY total_sales DESC) AS sales_rank
FROM ProductSales;
```
Output 1:

![image](https://github.com/user-attachments/assets/88ea9c33-93b3-4e65-b3b4-d5e7ff2d63b3)

```sql
-- Query 2: Customer Ranking by Total Purchase Amount

WITH CustomerSales AS (
    SELECT c.customer_id, CONCAT(c.first_name, ' ', c.last_name) AS customer_name, SUM(s.sales) AS total_purchase
    FROM Sales s
    JOIN Customers c ON s.customer_id = c.customer_id
    GROUP BY c.customer_id, customer_name
)
SELECT customer_id, customer_name, total_purchase,
       RANK() OVER (ORDER BY total_purchase DESC) AS purchase_rank
FROM CustomerSales;
```
Output 2:

![image](https://github.com/user-attachments/assets/d8ec3a72-f6de-46aa-bc73-f5a684bb7b0d)

```sql
-- Query 3: Products with Sales Above Average

SELECT p.product_id, p.product_name, SUM(s.sales) AS total_sales
FROM Sales s
JOIN Products p ON s.product_id = p.product_id
GROUP BY p.product_id, p.product_name
HAVING SUM(s.sales) > (
    SELECT AVG(total_sales) FROM (
        SELECT SUM(s.sales) AS total_sales
        FROM Sales s
        JOIN Products p ON s.product_id = p.product_id
        GROUP BY p.product_id
    ) subquery
);
```
Output 3:

![image](https://github.com/user-attachments/assets/e3627282-c6dc-41b1-8b02-edd4fa10bbd3)

**Supporting Documents**<br>
Get the full report [here](https://github.com/randycampher/rainbow_retail_analysis/blob/main/Data%20Analysis%20Report.pdf) <br>
Access the presentation to stakeholders [here](https://github.com/randycampher/rainbow_retail_analysis/blob/main/Presentation.pdf) <br>





