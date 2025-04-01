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
2. POWER QUERY
3. ZOOM CHART Guide about vizual 


