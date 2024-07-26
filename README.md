# RAINBOW RETAIL
# Data Analysis Report: Sales Performance 2018-2022

| **Section**                            | **Details**                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Executive Summary**                  | This report evaluates Rainbow Retail's sales performance from 2018 to 2022. <br>The analysis, based on synthetic data, highlights key trends and offers actionable insights to optimise future business strategies.<br> Key findings include a consistent upward trend in sales and revenue, with technology products leading the market share. <br>Strategic recommendations are provided to enhance product portfolio, marketing strategies and regional sales efforts, aligned with broader business goals such as market expansion, product diversification and customer retention.                        |
| **Introduction**                       | Rainbow Retail, a South African e-commerce retailer specialising in office supplies, furniture and technology products, aims to leverage data insights to refine its sales strategy and improve market position. <br>This report outlines the current sales performance and identifies strategic opportunities for growth and optimisation.                                                                                                                                             |
| **Data Overview**                      | <br> ![image](https://github.com/user-attachments/assets/3b9dcc14-d978-404d-b366-611e484ba282) <br>The analysis uses synthetic data representing customers, sales, products and temporal entities, allowing for comprehensive tracking of sales transactions and trends. The data spans from January 2018 to December 2022. |
| **Analysis**                           | **Sales and Revenue Growth Trend** <br> ![image](https://github.com/user-attachments/assets/c200ebbf-69ba-4a02-8f41-0ff927f82c20)<br> *Insight*: A general upward trajectory in monthly sales and revenue indicates robust growth. <br> *Strategic Goal*: Market Expansion. Capitalise on the growth trend by exploring new market segments and expanding product lines to maintain momentum. <br><br> **Product Category Performance** <br> ![image](https://github.com/user-attachments/assets/2856899c-60e8-4cc5-9433-e10335545f52) <br> *Insight*: Technology products dominate with 49% of total revenue, while the furniture category underperforms at 3%. <br> *Strategic Goal*: Product Diversification. Expand the range of technology products and enhance the promotion of underperforming categories like furniture to reduce dependency on a few product lines. <br><br>  **Top-Selling Products** <br> ![image](https://github.com/user-attachments/assets/02da6bd8-5f02-43ed-881d-3f0f233aa47c) <br> *Insight*: A few key products, like the High-Speed Automatic Electric Letter Opener, drive significant sales. <br>*Strategic Goal*: Revenue Maximisation. Develop upselling and cross-selling strategies around these top-performing products to boost the Average Order Value (AOV) and overall revenue. <br><br>  **Sales by Province** <br> ![image](https://github.com/user-attachments/assets/1daefab2-5582-4575-909d-dbf7724c8eb0) <br> *Insight*: KwaZulu-Natal, Gauteng and Eastern Cape are leading markets, with potential growth opportunities in Limpopo and Northern Cape. <br>*Strategic Goal*: Geographical Expansion. Focus marketing efforts on underperforming regions to balance sales distribution and enhance overall market penetration. <br><br>  **Average Order Value (AOV)** <br> *Insight*: The AOV stands at R4,467, providing insights into purchasing behavior. <br>*Strategic Goal*: Customer Retention and Value Enhancement. Implement targeted marketing campaigns and "smart shopper" programmes to encourage higher spending and repeat purchases.|  
| **Recommendations**                    | **Product Portfolio Optimisation** <br> - Expand the technology product line and consider strategic partnerships to boost the furniture category. <br> - Investigate unclassified products to identify emerging market trends and opportunities for new product categories.<br><br> **Sales and Marketing Strategy Enhancement** <br> - Intensify marketing efforts in high-performing regions and develop targeted campaigns in regions with growth potential. <br>- Use insights from AOV analysis to tailor product bundles and promotional offers. <br><br>**Data Analysis and Reporting Enhancement** <br> - Improve data categorisation to ensure accurate reporting and deeper customer behavior analysis, assisting in more informed strategic decisions. |
| **Assumptions**                        | Data completeness issues, such as the significant portion of revenue from unclassified categories, may impact the accuracy of the analysis.                                                                                                                                                           |
| **Technical Approach**                 | The analysis utilised advanced Excel features such as Power Query and Power Pivot and SQL for data extraction, transformation and loading. This approach facilitated comprehensive data analysis and insightful reporting.                                                                                                                                                                                     |
| **Conclusion**                         | By implementing these strategic recommendations, Rainbow Retail can enhance its sales performance, optimise product offerings and strengthen its market presence. Aligning data insights with strategic business goals will ensure sustained growth and competitive advantage in the South African e-commerce market.                                                                                                        |

<br> **Ad-Hoc Queries** <br> Use of SQL queries to answer "on-the-go" questions by management. | 

```

sql -- Query 1: Top Products by Total Sales Amount

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

```
sql
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

```
sql
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





Get the full report [here](https://github.com/randycampher/rainbow_retail_analysis/blob/main/Data%20Analysis%20Report.pdf) <br>
Access the presentation to stakeholders [here](https://github.com/randycampher/rainbow_retail_analysis/blob/main/Presentation.pdf) <br>





