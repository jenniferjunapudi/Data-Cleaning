# Sales Dashboard

### Summary
The sales dashboard project was created to enhance internet sales reporting by moving from static reports to dynamic visual dashboards. The dashboard tracks sales by product and customer, alows filtering by sales representatives, and compares perfomance against the budget. Data was cleansed and transformed using SQL, and the resulting Power BI dashboard provides a comprehensive view of sales trends, enabling bettera nalysis and decision-making for sales managers and representatives.

### Business Request & User Stories
#### Business Request
Sales Manager:
We need to improve our internet slaes reports and want to move from static reports to visual dashboards. Essentially, we want to focus ti on how much we have sold of what products, to which clients and how it has been over time. Seeing as each sales person works ond ifferent products and customers it would be beneficial to be able to filter them also. We measure our numbers against budget so I added that in a spreadsheet so we can compare our values against performance. The budget is for 2021 and we usually look 2 years back in time when we do analysis of slaes. Let me know if you need anything else!

#### User Stories
As a result of the received request, the following stories were created:
| # | As a (role)             | I want (request/demand)                     | So that I (user value)                  | Acceptance Criteria                        |
|---|-------------------------|---------------------------------------------|-----------------------------------------|--------------------------------------------|
| 1 |Sales Manager            | To get a dashboard overview of internet sales| Can follow better which customers and products sells the best| A Power BI dashboard which updates data once a day.
| 2 | Sales Representative| A detailed overview of Internet Sales per Customers| Can follow up with my customers who buy the most and who we can sell more to | A Power BI dashboard which allows me to filter data for each customer|
| 3 | Sales Representative| A detailed overview of Internet Sales per Product|Can follow up my Products that sell the most | A Power BI dashboard which allows me to filter data for each Product.|
| 4 | Sales Manager | A dashboard overview of internet sales | A dashboard overview of internet sales | Follow sales over time against budget | A Power BI dashboard with graphs and KPIs comparing against budget. | 


#### Tools and Libraries Used
- **MSSQL (SQL Server Management Studio) (SSMS)**
- **Microsoft Power BI**


#### Data Cleaning & Transformation (SQL)
To create the necessary data model for the analysis to fulfill the business needs, the following tables were extracted using SQL. 

One data source (sales budgets) was provided in Excel format and was connected to the data model after initial cleansing.

Below are the SQL statements for cleansing and transforming necessary data.

```
Code
```


#### Data Model
The subsequent data model was produced

#### Sales Management Dashboard
The finished slaes management dashboard with one page works as a dashboard and overview, with two other pages focused on combining tables for necessary details and visualizations to show sales over time, per customer, and product.
