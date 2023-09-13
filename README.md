# Project-Sales-Dashboard
The data, content, and final delivery I shared on GitHub utilize mock-up data due to confidentiality. This work sample aims to demonstrate my analytical skills, problem-solving approach, and the lessons I learned from the case.

### Table of contents
* [1. Introduction](#1)
* [2. Specifications](#2)
* [3. Dataset](#3)
* [4. Data Model](#4)
* [5. Results](#5)
    * [Proof of Concept Dadhboard Design](#5.1)
    * [Design Considerations - Assumptions](#5.2)
    * [Technical Challenges - Highlights](#5.3)
    * [Business Insights - Recommendations](#5.4)
    * [Lesson Learned](#5.5)

<a id="1"></a>
### 1. Introduction
The primary aim of this dashboard is to model, measure, analyze, and monitor the sales performance within the furniture department store. To achieve this, the Orders, People, and Returns datasets have been made accessible to extract valuable insights on sales and orders. Additionally, by employing predefined dimensions and key performance indicators, three different analysis will be generated, serving the information needs of various stakeholders.
<br />
<a id="2"></a>
### 2. Specifications
The analysis should encompass key measures such as the cost of goods sold, year-over-year sales growth by order date, sales amount discounted, consumer sales, amount returned, rolling 4-month sales by order date, the last refresh of the data model, and total sales by both month ordered and month shipped.<br />
<br />
The dashboard is composed of three pages: Sales Summary, Product Detail, and Customer Detail. The Sales Summary page is designed for the executive team, providing a high-level overview of year-over-year sales and gross margin performance trends compared to the previous year, segmented by product category, customer segment, time period, and region. Potential key performance indicators include sales amount, gross margin, and cost.<br />
<br />
The Product Detail page aims to assist the sales and marketing teams in gaining a deeper understanding of individual product performance, enabling them to refine operational strategies and deliver targeted campaigns.<br />
<br />
Lastly, the Customer Detail page is tailored for the CRM and marketing campaign department, offering insights into customer behaviors. It utilizes top N analysis to identify the most valuable customers and examines the contribution of each customer segment to the total sales amount.
<a id="3"></a>
### 3. Dataset
The dataset consists of a total of 9 tables, including 3 source data tables and 6 data mart tables.<br />
<br />
**Orders:**  This fact table contains information such as customer code, order code, order date, postal code, last product update, and product code  <br /> 
<br />
**People:** Provides information about person (cutomer name) and regions<br />
<br />
**Returns:** Contains data on order codes and indicates whether a product has been returned<br />
<br />
**Calender:** Includes a single record for each date used in the analysis<br />
<br />
**Customer:** Generated from the order table, it includes details such as customer code, customer name, and segment<br />
<br />
**Date Type:** Specifies the type of date, either order date or ship date<br />
<br />
**Last Refresh:** Each time the dashboard is refreshed, this table updates and returns the latest refresh time<br />
<br />
**Product:** Generated from the order table with a predefined filter, it includes product details such as product code, category, sub-category, product name, and last product update<br />
<br />
**Region:** Generated from the order table, this table contains information about postal code, country, state, city, and region<br />
<br />

<a id="4"></a>
### 4. Data Model <a name="data-model"></a>
![256943677-00345b6d-db02-4f3f-ae6f-92cf428ea6eb](https://github.com/hilxwang/Powe-BI-Sales-Retail-Dashboard/assets/96967687/80f2fcd5-23ad-43bb-87cb-6156d57d94d6)

<a id="5"></a>
### 5. Results
<a id="5.1"></a>
#### Proof of Concept Dadhboard Design
![Powe-BI-Sales-Retail-Dashboard_Page_1](https://github.com/hilxwang/Powe-BI-Sales-Retail-Dashboard/assets/96967687/f5ca3e85-7acc-4d64-8ef0-5953089f5a54)
![Powe-BI-Sales-Retail-Dashboard_Page_2](https://github.com/hilxwang/Powe-BI-Sales-Retail-Dashboard/assets/96967687/8064d548-6d32-4e52-83d9-9e84e65d48ac)
![Powe-BI-Sales-Retail-Dashboard_Page_3](https://github.com/hilxwang/Powe-BI-Sales-Retail-Dashboard/assets/96967687/dda40b68-8f50-4a55-81e1-9a3187ce6935)
![Powe-BI-Sales-Retail-Dashboard_Page_4](https://github.com/hilxwang/Powe-BI-Sales-Retail-Dashboard/assets/96967687/555d5c81-1781-40fe-a897-1ff23b1863cb)
<br />

<a id="5.2"></a>
#### Design Considerations - Assumptions
1. SCD: Product - Employing SCD techniques to manage changes in product data over time<br />
2. Postcode serves as the primary key in the Region hierarchy - Utilizing postcode as the unique identifier in the hierarchical structure of regions<br />
3. Data security implementation - Region managers granted access to specific regional KPIs based on their login credentials, ensuring restricted visibility aligned with their managerial responsibilities.
<br />

<a id="5.3"></a>
#### Technical Challenges - Highlights
1. Implement parameterized environmental variables for future deployments to enhance flexibility and adaptability.<br />
2. Utilized M code to incorporate the latest refresh time, ensuring up-to-date data for analysis and reporting.<br />
3. Developed custom functions for diverse purposes, enabling streamlined and efficient processes.
<br />

<a id="5.4"></a>
#### Business Insights - Recommendations
1. The Profit Rate metric is highly valuable for informing product purchasing and pricing strategies.<br />
2. Through the analysis of customers' shopping habits and their Gross Margin (%), the CRM team can effectively plan targeted campaigns for specific customers.<br />
3. The Return Rate serves as a useful key performance indicator for the product team, aiding in the formulation of product plans.
<br />

<a id="5.5"></a>
#### Lesson Learned

The lesson learned from the case emphasizes the value of effectively managing datasets to extract insights, utilizing dimensions, KPIs, and analysis techniques while considering the purpose and audience of each delivery. It underscores the significance of secure data access and customized reporting aligned with user roles. Leveraging data enables informed actions and enhances organizational performance.
