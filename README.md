# InventoryManagement
FP20 Analytics ZoomCharts Challenge

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

First of all, I chose type 16:9 in canvas settings according to requirements of the challenge. To present my main measures and calculation I added a vizualization that called card(new) and then added 5 my value. I colored this in black and did the same size of labels and text.
According to the main question of research to understand weather there are any seasonal trends when the highest number of products were restocked I decided to display this using vizualization called drill down combo pro (filter) because this kind of viz is the best for categorical data.

To identify the five most expensive product I voted in also drill down combo pro (filter) vizualization and did advanced filter by max of unit price to see five most expencive product

in order to understand which warehouse location has the highest number of products stored i made use column warehouse location and calculate the sum of stock quantity 

to display which country has the most stocked items, and which top 3 counties have the highest stocked quantities by different product categories i used drill down map pro (filter)

# Function and techniques
1. DAX - SUM, AVERAGE, ABS, VAR, COUNT, FIRSTNONBLANK, RETURN
2. POWER QUERY - GroupBY, Customer Column, Rounding, Column quality
3. ZOOM CHART Guide
   

# Conclusion 
1. The highest total stock quantity has "Home and Garden" category. In general stock quantity for all existing category is almost equal and indicate that company are keeping a balanced inventory without focusing too much on any one product category, which could mitigate risk. But it depends on demand on category because if the demand on certain category is not predictable and not stable then large level stock is unneeded and maybe company can bumb into over-investing and over0stocking. To understand this analyst need to analyse the quantity and data of product from all category and identify high-demand category and seasonal-category to optimize the level of stock

2. 262 products currently have stock quantities below their reorder point. In according to total stock quantity it is low quantity. But to avoid this company can research some patterns and reason why for all category at least 30 items is out of stock.

3. Minimum order quantity - 8163.The 8163 units the company need to restock account for only about 0.27% of your total inventory. This suggests that the scale of restocking is relatively small compared to your overall stock, which is a good sign that your inventory levels are well-managed in general. But again it depends on the demand of the kinds of products to prioritize restocking based on it and the level of critisism and priority.

4. The highest average lead time for restocking has supplier SUP041.

5. 179 days - average time since the last restock for products marked as "Out of Stock". The longer a product is out of stock, the more likely it is that customers will move to competitors. A period of 179 days could mean that company losing out on a significant amount of sales if these products are popular or essential. 

6. The highest number of products were restocked in July and October if we consider annual data, so we can suppose that it happens often in the middle of the year or in the end of the year.

8. The fastest turnover based on stock quantity and lead time has "Home and Garden" category. But in result of calculation we can see that all product category of company have demand but according to our stock quantity we can suggests that inventory is moving slowly.



# What could be done? 
If the result of analysis average lead time since the last restock for products marked as out of stock 179 days then it can be problematic. For company need to look at sourcing, order lead times, and shipping times to shorten the restock period or consider implementing safety stock policies, which ensure that there is always a buffer stock to prevent products from going out of stock for extended periods. In another words there is needs to optimize supply chain or Inventory Forecasting. Company can use forecasting techniques to predict demand more accurately, so that company will be prepared for restocking in advance.

To improve the turnover, company could reduce the number of units on hand to match your sales velocity more closely and optimize stock level, find ways to speed up the sales process, such as promotions, advertising, or even adjusting pricing to increase demand, identify which products have low sales velocity and consider moving them out of your inventory and reduce slow-moving products.



