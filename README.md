Kaggle's Dataset link: https://www.kaggle.com/datasets/rishikumarrajvansh/marketing-insights-for-e-commerce-company?select=Online_Sales.csv

** Inputs related to Analysis for additional reference:**

Why do we need customer Segmentation?
Every customer is unique and can be targeted in different ways. Customer segmentation
plays an important role in this case. The segmentation helps to understand the profiles of customers and
can help define cross-sell/upsell/activation/acquisition strategies.
What is RFM Segmentation?
RFM Segmentation is an acronym for recency, frequency, and monetary-based segmentation.
Recency is about when the last order of a customer. It means the number of days since a customer
made the last purchase. If it’s a case for a website or an app, this could be interpreted as the last
visit day or the last login time.
Frequency is about the number of purchases in a given period. It could be 3 months, 6 months or 1
year. So we can understand this value as for how often or how many customers use the product of
a company. The bigger the value is, the more engaged the customers are.
Alternatively
We can define, the average duration between two transactions
Monetary is the total amount of money a customer spent in that given period. Therefore big
spenders will be differentiated from other customers such as MVP or VIP.
What is LTV and How to define it?
In the current world, almost every retailer promotes its subscription and this is further used to
understand the customer lifetime. Retailers can manage these customers in a better manner if they
know which customers have high lifetime value.
Customer lifetime value (LTV) can also be defined as the monetary value of a customer relationship,
based on the present value of the projected future cash flows from the customer relationship.
Customer lifetime value is an important concept in that it encourages firms to shift their focus from
quarterly profits to the long-term health of their customer relationships. Customer lifetime value is
an important metric because it represents an upper limit on spending to acquire new customers. For
this reason, it is an important element in calculating the payback of advertising spent in marketing mix
modeling.
Why do need to predict Customer Lifetime Value?
The LTV is an important building block in campaign design and marketing mix management.
Although targeting models can help to identify the right customers to be targeted, LTV analysis can
help quantify the expected outcome of targeting in terms of revenues and profits. The LTV is also
important because other major metrics and decision thresholds can be derived from it.
For example, the LTV is naturally an upper limit on the spending to acquire a customer, and the sum
of the LTVs for all of the customers of a brand, known as customer equity, is a major metric for business valuations. Similarly to many other problems of marketing analytics and algorithmic
marketing, LTV modeling can be approached from descriptive, predictive, and prescriptive
perspectives.
How Does Next Purchase Day Help Retailers?
Our objective is to analyze when our customers will purchase products in the future so for such
customers, we can build strategies and come up with strategies and marketing campaigns
accordingly.
a. Group-1: Customers who will purchase in more than 60 days
b. Group-2: Customers who will purchase in 30-60 days
c. Group 3: Customers who will purchase in 0-30 days
What is Cohort Analysis? How it will be helpful?
A cohort is a group of users who share a common characteristic that is identified in this report by an
Analytics dimension.
For example, all users with the same Acquisition Date belong to the same cohort.
The Cohort Analysis report lets you isolate and analyze cohort behavior.
Cohort analysis in e-commerce means monitoring your customers’ behavior based on common
traits they share – the first product they bought, when they became customers, etc. - - to find
patterns and tailor marketing activities for the group.
Transaction data has been provided for the period of 1st Jan 2019 to 31st Dec 2019. The below data
sets have been provided.
Online_Sales.csv: This file contains actual order data (point of Sales data) at the transaction level with
below variables.
CustomerID: Customer unique ID
Transaction_ID: Transaction Unique ID
Transaction_Date: Date of Transaction
Product_SKU: SKU ID – Unique ID for the product
Product_Description: Product Description
Product_Cateogry: Product Category
Quantity: Number of items ordered
Avg_Price: Price per one quantity
Delivery_Charges: Charges for delivery
Coupon_Status: Any discount coupon applied
Customers_Data.csv: This file contains customer’s demographics.
CustomerID: Customer Unique ID
Gender: The gender of the customer
Location: Location of Customer
Tenure_Months: Tenure in Months
Discount_Coupon.csv: Discount coupons have been given for different categories in different
months
Month: Discount coupon applied in that month
Product_Category: Product category
Coupon_Code: Coupon Code for given Category and given month
Discount_pct: Discount Percentage for a given coupon
Marketing_Spend.csv: Marketing spends on both offline & online channels day-wise.
Date: Date
Offline_Spend: Marketing spend on offline channels like TV, Radio, Newspapers, Hoardings, etc
Online_Spend: Marketing spend on online channels like Google keywords, Facebook, etc
Tax_Amount.csv: GST Details for a given category
Product_Category: Product Category
GST: Percentage of GST
**
Key Definitions:**
Invoice Value: Invoice Value =(( QuantityAvg_price)(1-Dicount_pct)*(1+GST))+Delivery_Charges
Average order value = Revenue / Transaction per customer
Profit Margin Profit margin is the commonly used profitability ratio. It represents how much
percentage of total sales has earned as the gain.
Purchase Frequency is the average number of purchases made by a customer over a defined period (typically one month or one year). It is the sum of the total number of transactions divided by the total
number customers.
Repeat rate shows you the percentage of your current customer base that has come back to shop
again.
Churn Rate is the annual percentage rate at which customers stop subscribing.
Customer lifetime value, lifetime customer value, or lifetime value is a prediction of the net
profit/revenue attributed to the entire future relationship with a customer.

Business Objective:
The e-commerce company is expecting below analysis using the data

Calculate the Invoice amount or sale_amount or revenue for each transaction and item level
 Invoice Value =(( QuantityAvg_price)(1-Dicount_pct)*(1+GST))+Delivery_Charges
Perform Detailed exploratory analysis
 Understanding how many customers are acquired every month
 Understand the retention of customers on month on month basis
 How are the revenues from existing/new customers on the month on monthly basis
 How do the discounts play a role in the revenues?
 Analyse KPIs like Revenue, number of orders, average order value, number of
customers (existing/new), quantity, by category, by month, by week, by day, etc
 Understand the trends/seasonality of sales by category, location, month, etc
 How number orders and sales are on different days?
 Calculate the Revenue, Marketing spend, and percentage of marketing spend out of
revenue, Tax, percentage of delivery charges by month.
 How is marketing spending impacting revenue?
 Which product has appeared in the transactions?
 Which product was purchased mostly based on the quantity?
Performing Customer Segmentation
 Heuristic (Value based, on RFM) – Divide the customers into Premium, Gold, Silver,
Standard customers and define strategy on the same.
 Scientific (Using K-Means) & Understand the profiles. Define strategy for each
segment.
Predicting Customer Lifetime Value (Low Value/Medium Value/High Value)
 First define the dependent variable with categories low value, medium value, high value
using customer revenue.
 Then perform the Classification model
Cross-Selling (Which products are selling together)
 You can perform exploratory analysis & market basket analysis to understand which
of items can be bundled together.
Predicting Next Purchase Day(How soon each customer can visit the store (0-30 days, 30-60
days, 60-90 days, 90+ days)
 For this, we need to create a dependent variable at the customer level (average days per one
transaction for only repeat customers and divide into groups 0-30 days, 30-60 days,
60-90 days and 90+ days) then build a classification model to predict the next purchase of
given customer.
Perform cohort analysis by defining below cohorts
 Customers who started each month and understand their behavior
 Which Month cohort has maximum retention?
