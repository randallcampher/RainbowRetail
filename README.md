# rainbow_retail_analysis
Sales trend analysis for fictitious e-commerce company 

| **EXECUTIVE SUMMARY** |
|-----------------------|
| This project evaluates Rainbow Retail's sales performance from 2018 to 2022, highlighting key trends and providing actionable insights for future strategies. The analysis uses synthetic data, including customers, sales, products and calendar entities. |

| **a. Key Findings** |
|------------------|
| **Sales and Revenue Growth:** Consistent growth in sales and revenue with technology products driving 49% of total revenue. Office supplies contributed 33%, while furniture underperformed at 3%. |
| **Product Performance:** Top products like the High-Speed Automatic Electric Letter Opener and Cisco Telepresence System EX90 dominate. This indicates a need for product diversification and enhanced promotion of underperforming items. |
| **Regional Sales Analysis:** Key markets are KwaZulu-Natal, Gauteng and Eastern Cape, with growth potential in Limpopo and Northern Cape. Opportunities exist for market expansion and resource optimisation. |
| **Average Order Value (AOV):** The AOV is R4,467, suggesting opportunities for upselling and cross-selling. |

| **b. Recommendations** |
|---------------------|
| **Product Portfolio Optimisation:** Expand technology products, review the underperforming furniture line and explore unclassified categories for growth. |
| **Sales and Marketing Strategies:** Focus on high-performing regions, target low-performing areas and develop strategies to increase AOV. |
| **Seasonal Sales Optimisation:** Analyse seasonal sales trends and implement dynamic pricing strategies. |
| **Data Analysis Enhancement:** Improve product categorisation, analyse customer behaviour and refine data collection. |

| **c. Technical Approach** |
|------------------------|
| Utilised SQL and advanced Excel features such as Power Query and Power Pivot for data extraction, transformation, loading and analysis. |


## 1. INTRODUCTION
Rainbow Retail is a fictitious South African e-commerce retailer of office supplies, furniture and technology products. This report aims to evaluate sales performance, identify trends and provide actionable insights.

## 2. DATA OVERVIEW
### a. Data Sources
Synthetic data includes four primary entities: Customers, Sales, Products and Calendar, enabling comprehensive tracking and analysis.

![image](https://github.com/user-attachments/assets/90a8f40d-8336-4e9e-95cb-96fa8e91d87f)

*Key aspects:*
- **Customers:** Essential details for segmentation and targeted marketing.
- **Sales:** Central repository for transactions, linking customers to products.
- **Products:** Categorises inventory to support performance evaluations.
- **Calendar:** Facilitates time-based analysis.

*Time Frame:* 01 January 2018 – 31 December 2022

## 3. Analysis
### a. Sales and Revenue Growth Trend

![image](https://github.com/user-attachments/assets/0810efbf-d28d-46b0-b4fb-442ef51022e8)

- **General Trend:**
  - Line graphs for monthly sales and revenue from 2018 to 2022 show a general upward trajectory.
  - Indicates consistent growth over the five-year period, suggesting overall positive performance.

- **Key Observations:**
  - Noticeable fluctuations within the upward trend.
  - Possible reasons for fluctuations:
    - Seasonal variations in consumer spending patterns
    - Impact of specific market events or economic conditions on sales performance

- **Further Analysis:**
  - Analysing these fluctuations could provide valuable insights into market dynamics and consumer behavior.


### b. Product Category Performance

![image](https://github.com/user-attachments/assets/be791e3f-d565-4ad1-9c25-f00ac3ac53f4)

- **Dominant Category:**
  - Technology products dominate revenue generation, contributing a substantial 49% of total revenue.

- **Secondary Category:**
  - Office Supplies follow as the second-largest contributor at 33%.

- **Notable Findings:**
  - Unclassified categories account for 15% of revenue, warranting further investigation.
  - Anomaly detected: Furniture category underperforms significantly, contributing only 3% to overall revenue.

- **Insights:**
  - The distribution highlights a heavy reliance on technology products, indicating a strong market position in this sector.
  - Suggests a need for diversification to reduce dependency on a single category.


### c. Top-Selling Products

![image](https://github.com/user-attachments/assets/a7fdbf50-b250-48b2-9e02-b60ad5bf8978)

- **Top Performers:**
  - High-Speed Automatic Electric Letter Opener leads in sales, generating R1,466,247.
  - Cisco Telepresence System EX90 follows closely with R1,256,436 in sales.

- **Product Diversification:**
  - The product range includes a mix of office equipment, high-end technology systems and furniture, suggesting a diverse product portfolio.

- **Sales Distribution:**
  - The leading products significantly outperform others, indicating a reliance on a few key products for revenue.
  - Suggests a need to diversify product offerings or enhance promotion of lower-performing items.

- **Market Trends:**
  - High sales of office equipment like the letter opener and telepresence system suggest strong demand in the business and corporate sectors.

- **Opportunities for Growth:**
  - Potential to increase marketing efforts for mid and lower-tier products, especially those that complement top-selling items.


### d. Sales by Province

![image](https://github.com/user-attachments/assets/b568df9f-f192-4fb6-9465-658d4d50590d)

- **Regional Focus:**
  - KwaZulu-Natal, Gauteng and Eastern Cape are key markets.
  - These provinces should be the focus of intensified marketing and sales strategies to capitalise on existing demand.

- **Growth Opportunities:**
  - Provinces with lower sales, such as Limpopo and Northern Cape, present opportunities for targeted marketing campaigns and promotional activities to boost sales.

- **Market Expansion:**
  - The variance in sales figures across provinces suggests potential for expansion in underperforming regions.
  - Consider market research to understand local consumer behavior and needs.

- **Resource Allocation:**
  - Data can guide resource allocation, such as sales team deployment and inventory distribution, ensuring alignment with demand patterns.


### e. Average Order Value (AOV)

- **Current AOV:**
  - The average order value stands at R4,467 over the observed period.
  - Provides insight into the typical purchasing power and behavior of customer base.

- **Trends to Investigate:**
  - How this AOV compares to industry standards.
  - Evolution of AOV over time.

- **Potential Anomaly:**
  - If this AOV significantly differs from industry benchmarks, it could indicate unique market positioning or specific customer segment targeting.


### f. Ad-Hoc Queries

The SQL snippets below answer some common business questions asked by stakeholders. 

```
sql
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

## 4. RECOMMENDATIONS

### Sales and Marketing Departments

- **Intensify Regional Marketing:**
  - Focus on key markets like KwaZulu-Natal, Gauteng and Eastern Cape where demand is high.
  - Develop targeted marketing campaigns for underperforming regions such as Limpopo and Northern Cape to boost sales.

- **Promote Product Diversification:**
  - Enhance promotional efforts for lower-performing items, particularly those that complement top-selling products like office equipment and high-end technology systems.

- **Seasonal and Event-based Campaigns:**
  - Utilise data on seasonal sales fluctuations to time campaigns effectively, maximising revenue during peak periods.

### Product and Procurement Departments

- **Expand Product Range:**
  - Consider introducing new products or categories to reduce reliance on technology products, which currently dominate revenue.

- **Investigate Unclassified Categories:**
  - Further analyse the 15% revenue from unclassified categories to identify potential new product lines or niches.

- **Address Underperforming Categories:**
  - Explore reasons behind the low performance of the furniture category and develop strategies to improve sales, such as product redesign or repositioning.

### Finance and Strategy Departments

- **Analyse Average Order Value (AOV):**
  - Compare AOV of R4,467 with industry benchmarks to assess market positioning.
  - Investigate trends in AOV over time to understand changes in customer purchasing behavior.

- **Resource Allocation:**
  - Use sales data to optimise resource allocation, ensuring that sales teams and inventory are aligned with demand patterns in different regions.

### Customer Relations and Service Departments

- **Customer Feedback on Product Range:**
  - Gather customer insights on existing products and potential new offerings, particularly focusing on the office supplies and technology sectors.

- **Enhance Customer Experience:**
  - Improve after-sales support for high-value items like the Cisco Telepresence System EX90 to maintain customer satisfaction and loyalty.

### Research and Development (R&D) Department

- **Market Research:**
  - Conduct market research in regions with lower sales to better understand local consumer preferences and tailor offerings accordingly.

- **Trend Analysis:**
  - Analyse sales data for emerging trends, such as increasing demand for specific product types, to inform product development and marketing strategies.

These recommendations are designed to align each department's efforts with the overall strategic goals of Rainbow Retail, fostering growth and enhancing market competitiveness.


## 5. ASSUMPTIONS
Data completeness issues, particularly with unclassified categories, may affect insights.

## 6. TECHNICAL
- **Excel:** Advanced features including Power Query and Power Pivot for ETL and EDA.
- **SQL:** For sophisticated data querying and insight extraction.

## 7. CONCLUSION
Implementing these recommendations will enhance Rainbow Retail's sales performance, optimise product offerings and strengthen market presence for sustainable growth in the South African e-commerce market.

Get the full report [here](https://github.com/randycampher/rainbow_retail_analysis/blob/main/Data%20Analysis%20Report.pdf)
Access the presentation to stakeholders [here](https://github.com/randycampher/rainbow_retail_analysis/blob/main/Presentation.pdf)




