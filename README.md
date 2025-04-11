# InventoryManagement
FP20 Analytics ZoomCharts Challenge

Link: https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/fp20-analytics-april-2025

# Project

This challenge explores key aspects such as stock levels, supplier performance, warehouse utilisation, and reorder strategies. By analysing this dataset, you will identify trends, optimise restocking, and assess cost efficiency. The primary goal of this project was uncovering actionable insights that enhance inventory operations and decision-making



# Terms and definitions 

1) Product_ID	>> Unique identifier for the product
2) Product_Name >>	Name of the product
3) Category >>	Category to which the product belongs
4) Unit_Price >>	Price per unit of the product
5) Stock_Quantity >>	Quantity of the product available in stock
6) Stock_Level	>> Stock level category (e.g., Low, Medium, High)
7) Reorder_Point	>> Minimum quantity at which reordering is triggered
8) Lead_Time_Days >>	Number of days it takes to receive the product after ordering
9) Last_Restock_Date	>> Date when the product was last restocked
10) Supplier_ID	Unique >> identifier for the product supplier
11) Warehouse_Location >>	Location of the warehouse storing the product
12) Min_Order_Quantity >>	Minimum quantity that must be ordered when placing a restock
13) Status>>	Current status of the product (e.g., Active, Discontinued)
14) Entry_Date >>	Date the product entry was added to the system
15) Country >>	Country where the product is stored or distributed
16) Latitude >>	Latitude coordinate of the warehouse location
17) Longitude >>	Longitude coordinate of the warehouse location





# Questions: 

Stock Analysis & Inventory Levels
1. Which product category has the highest total stock quantity across all products?
2. How many products currently have stock quantities below their reorder point?
3. What minimum order quantity is required for a company to restock all products below the reorder point?


Supplier & Restocking Performance

4. Which supplier has the highest average lead time for restocking?
5. What is the average time since the last restock for products marked as "Out of Stock"?
6. Identify the months when the highest number of products were restocked - are there any seasonal trends?


Cost & Pricing Analysis

7. Identify the top 5 most expensive products (by unit price) and their categories.
8. Which product category has the fastest turnover based on stock quantity and lead time?



Warehouse & Geographic Insights

9. Which warehouse location has the highest number of products stored?
10. Which country has the most stocked items, and which top 3 counties have the highest stocked quantities by different product categories?


# Main stages 
1.Identified the data source to be used and imported the dataset in Power BI

2.Researched of the dataset for duplicates and for missing values - cleaned and then transformed data into a usable variant

3.Build data models in Power BI using tables, relationships, calculated columns, and measures

4.Found the answer on the questions of projects (you can find the DAX solution in file queries.dax)

5.Report Design

First of all, I selected the 16:9 aspect ratio in the canvas settings according to the requirements of the challenge. To present my main measurements and calculations, I added a visualization called "Card (New)" and then included my five values. I colored this black and ensured that the labels and text were the same size.

To address the main research question—whether there are any seasonal trends in the restocking of products—I decided to display this using a visualization called "Drill Down Combo Pro (Filter)" because this type of visualization is best suited for categorical data.

To identify the five most expensive products, I also used the "Drill Down Combo Pro (Filter)" visualization and applied an advanced filter to show the top five products with the highest unit prices.

In order to understand which warehouse location has the highest number of products stored, I used the "Warehouse Location" column and calculated the sum of the stock quantities.

To display which country has the most stocked items, and to identify the top three countries with the highest stocked quantities across different product categories, I used the "Drill Down Map Pro (Filter)" visualization.

# Function and techniques
1. DAX - SUM, AVERAGE, ABS, VAR, COUNT, FIRSTNONBLANK, RETURN
2. POWER QUERY - GroupBY, Customer Column, Rounding, Column quality
3. ZOOM CHART Guide
   

# Conclusion 
1. The highest total stock quantity is in the "Home and Garden" category. Overall, the stock quantity for all existing categories is almost equal, which indicates that the company is maintaining a balanced inventory without focusing too much on any one product category. This approach could mitigate risk. However, it depends on the demand for each category. If the demand for a certain category is unpredictable and unstable, having a large stock level may be unnecessary. The company might end up over-investing and overstocking. To address this, the analyst should examine the product quantities and data across all categories, identify high-demand and seasonal categories, and optimize stock levels accordingly.

2. Currently, 262 products have stock quantities below their reorder point. Although this number seems low in relation to total stock quantity, the company should investigate patterns and reasons why at least 30 items are out of stock in every category.

3. The minimum order quantity is 8,163 units. These 8,163 units that the company needs to restock account for only about 0.27% of total inventory. This suggests that the scale of restocking is relatively small compared to the overall stock, which is a positive sign that inventory levels are well-managed. However, restocking priorities should still be based on product demand and the urgency of each product.

4. The highest average lead time for restocking is with supplier SUP041.

5. The average time since the last restock for products marked as "Out of Stock" is 179 days. The longer a product is out of stock, the more likely customers will turn to competitors. A 179-day period could mean the company is losing a significant amount of sales if these products are popular or essential.

6. The highest number of products were restocked in July and October, based on annual data. This suggests that restocking often happens in the middle and at the end of the year.

8. The fastest turnover based on stock quantity and lead time is in the "Home and Garden" category. However, the calculation results show that all product categories have demand. Based on current stock quantities, we can suggest that inventory is moving slowly overall.





# What could be done? 
If the average lead time since the last restock for products marked as out of stock is 179 days, this could be problematic. The company needs to evaluate its sourcing, order lead times, and shipping times to shorten the restock period. Additionally, implementing safety stock policies could help ensure there is always a buffer to prevent products from being out of stock for extended periods. In other words, the supply chain and inventory forecasting processes need to be optimized. The company could use forecasting techniques to predict demand more accurately, allowing for more proactive restocking.

To improve turnover, the company could reduce the number of units on hand to better match sales velocity and optimize stock levels. The company should also explore ways to speed up the sales process, such as through promotions, advertising, or adjusting pricing to increase demand. Additionally, it would be helpful to identify products with low sales velocity and consider removing them from inventory to reduce slow-moving stock.



