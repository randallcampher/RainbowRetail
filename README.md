# rainbow_retail_analysis
Sales trend analysis for fictitious e-commerce company 

## EXECUTIVE SUMMARY

This project evaluates Rainbow Retail's sales performance from 2018 to 2022, highlighting key trends and providing actionable insights for future strategies. The analysis uses synthetic data, including customers, sales, products and calendar entities.

### Key Findings
- **Sales and Revenue Growth:** Consistent growth in sales and revenue with technology products driving 49% of total revenue. Office supplies contributed 33%, while furniture underperformed at 3%.
- **Product Performance:** Top products like the High-Speed Automatic Electric Letter Opener and Cisco Telepresence System EX90 dominate. This indicates a need for product diversification and enhanced promotion of underperforming items.
- **Regional Sales Analysis:** Key markets are KwaZulu-Natal, Gauteng and Eastern Cape, with growth potential in Limpopo and Northern Cape. Opportunities exist for market expansion and resource optimisation.
- **Average Order Value (AOV):** The AOV is R4,467, suggesting opportunities for upselling and cross-selling.

### Recommendations
- **Product Portfolio Optimisation:** Expand technology products, review the underperforming furniture line and explore unclassified categories for growth.
- **Sales and Marketing Strategies:** Focus on high-performing regions, target low-performing areas and develop strategies to increase AOV.
- **Seasonal Sales Optimisation:** Analyse seasonal sales trends and implement dynamic pricing strategies.
- **Data Analysis Enhancement:** Improve product categorisation, analyse customer behavior and refine data collection.

### Technical Approach
Utilised advanced Excel features and MySQL for data extraction, transformation, loading and analysis.

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

- **Trend:** Upward trajectory in sales and revenue with fluctuations, possibly due to seasonal variations or market events.

### b. Product Category Performance

![image](https://github.com/user-attachments/assets/be791e3f-d565-4ad1-9c25-f00ac3ac53f4)

- **Revenue Distribution:** Technology products (49%), Office Supplies (33%), Furniture (3%). Notable 15% from unclassified categories.

### c. Top-Selling Products

![image](https://github.com/user-attachments/assets/a7fdbf50-b250-48b2-9e02-b60ad5bf8978)

- **Top Performers:** High-Speed Automatic Electric Letter Opener (R1,466,247), Cisco Telepresence System EX90 (R1,256,436). Suggests a need for diversification and marketing of lower-performing items.

### d. Sales by Province

![image](https://github.com/user-attachments/assets/b568df9f-f192-4fb6-9465-658d4d50590d)

- **Key Markets:** KwaZulu-Natal, Gauteng, Eastern Cape. Growth opportunities in Limpopo and Northern Cape.

### e. Average Order Value (AOV)
- **Value:** R4,467. Investigate how this compares to industry standards and trends.

### f. Ad-Hoc Queries

The SQL queries below are added to simulate the application of SQL to databases in order to answer some common business questions by stakeholders. 

![image](https://github.com/user-attachments/assets/31fe9682-7467-4599-b7b6-ed117d78184b)

![image](https://github.com/user-attachments/assets/78e917a4-eea8-438e-b582-45677c74e1fd)

![image](https://github.com/user-attachments/assets/e7de645b-bccd-450e-8018-9d9589759246)

## 4. RECOMMENDATIONS

### Product Portfolio Optimisation (For Product Management and Sales Teams)
- Leverage the strong performance of the Technology category by expanding the range of technology products offered.
- Investigate opportunities for bundling technology products with complementary items from other categories.
- Address the underperformance of the Furniture category by conducting a thorough review of the furniture product line.
- Consider repositioning, repricing, or potentially phasing out underperforming furniture items.

### Category Expansion and Refinement (For Product Development and Marketing Teams)
- Investigate the 15% revenue from unclassified categories:
  - Analyse these products to identify emerging trends or niche markets.
  - Consider creating new formal categories based on this analysis.
- Develop strategies to grow the Furniture category:
  - Research market demands and trends in office and home furniture.
  - Explore partnerships with popular furniture brands or designers.

### Sales Strategy Enhancement (For Sales and Marketing Departments)
- Capitalise on the strong performance of office supplies:
  - Develop targeted marketing campaigns for top-selling office supply products.
  - Investigate cross-selling opportunities, pairing office supplies with technology products.
- Implement strategies to increase the Average Order Value:
  - Train sales staff on upselling techniques.
  - Create attractive bundle offers combining products from different categories.

### Seasonal Sales Optimisation (For Sales, Marketing, and Inventory Management Teams)
- Analyse the fluctuations in sales and revenue trends:
  - Identify peak and off-peak seasons.
  - Develop tailored marketing and inventory strategies for different seasons.
- Implement dynamic pricing strategies:
  - Adjust prices based on seasonal demand to maximize revenue during peak periods and maintain sales during slower periods.

### Data Analysis and Reporting Enhancement (For Business Intelligence and IT Departments)
- Improve product categorisation:
  - Develop a more comprehensive categorization system to reduce the 'unclassified' portion.
  - Regularly review and update product categories to ensure accuracy.
- Conduct deeper analysis on customer purchasing behaviour:
  - Investigate factors influencing the Average Order Value.
  - Segment customers based on purchasing patterns and develop targeted strategies for each segment.



## 5. ASSUMPTIONS
Data completeness issues, particularly with unclassified categories, may affect insights.

## 6. TECHNICAL
- **Excel:** Advanced features including Power Query and Power Pivot for ETL and EDA.
- **MySQL:** For sophisticated data querying and insight extraction.

## 7. CONCLUSION
Implementing these recommendations will enhance Rainbow Retail's sales performance, optimize product offerings, and strengthen market presence for sustainable growth in the South African e-commerce market.




