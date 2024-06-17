# Project 2: Power_BI_Superstore_Sales
# I. Introduction
## 1. Business requirements
Superstore is an global retail company. The head of Sales department wanted to know about current sales situation. Hence, he will ideate the appropriate strategies to choose strategic products and expand the market share. 


## 2. Business analysis using Design thinking 
### 2.1 Empathise
<img width="629" alt="image" src="https://github.com/mistletoegoegoe/Power_BI_Superstore_Sales/assets/121160527/2a1604c6-fd0e-41aa-9ae2-5fa3da12bfe2">

### 2.2 Define
<img width="629" alt="image" src="https://github.com/mistletoegoegoe/Power_BI_Superstore_Sales/assets/121160527/8a408a6f-2f37-496c-82fd-5d3af06ba738">

### 2.3 Ideate
<img width="677" alt="image" src="https://github.com/mistletoegoegoe/Power_BI_Superstore_Sales/assets/121160527/65a8c55b-8846-466b-bc14-f179f4584ac7">

### 2.4 Prototype and review
<img width="680" alt="image" src="https://github.com/mistletoegoegoe/Power_BI_Superstore_Sales/assets/121160527/466f9474-aa0d-4702-9b74-14e48d48af59">

## 3. Data dictionary
There are 3 data tables: 
- Orders: it was the fact table that contained all relevant information about each order_ID. It comprised time-related attributes, customer's information, market area, product details
- People: it contained name of salemen and the region that they were in charge of. 
- Returns: this table recorded the data about returned orders
### Table Orders
| Field          | Meaning                               |
|----------------|---------------------------------------|
| Order ID       | Unique ID of each order               |
| Order Date     | The date that order had been made     |
| Ship Date      | The date that order had been shipped  |
| Ship Mode      | The type of shipment                  |
| Customer ID    | Unique ID of customer                 |
| Customer Name  | Name of customer                      |
| Segment        | Customer segmentation                 |
| City           | City where order had been made        |
| State          | State where order had been made       |
| Country        | Country where order had been made     |
| Postal Code    | Postal code where order had been made |
| Market         | Market area of the order              |
| Region         | Region of order                       |
| Product ID     | Product unique ID in the order        |
| Category       | Category of product                   |
| Sub-Category   | Sub-category of product               |
| Product Name   | Product name                          |
| Sales          | Total revenue of order                |
| Quantity       | Total quantity of products in order   |
| Discount       | % discount for the order              |
| Profit         | Profit of the order                   |
| Shipping Cost  | Shipping cost for the order           |
| Order Priority | The level of priority                 |

### Table People
| Field  | Meaning                            |
|--------|------------------------------------|
| Person | The saleman who was in charge of   |
| Region | The region he/she was in charge of |

### Table Returns
| Field    | Meaning                               |
|----------|---------------------------------------|
| Returned | Yes/no - the status of returned order |
| Order ID | Unique ID of the order                |
| Market   | The market that had returned order    |
# II. Data visualisation
## 1. DAX
By the given data, there is no available Sales per order metric, which was necessary to provide an overview about Sales situation. Thus, a measure was created to calculate this indicator. The calculation would be implemented in DAX.
### Sales per order formula:
Sales per order = Total sales / Total orders
### DAX code
```
Sales per order = round((divide(sum(Orders[Sales]),DISTINCTCOUNT(Orders[Order ID]))),2)
```
## 2. Dashboard
## 3. Insights
## 4. Recommendations
