# Data-Cleaning & Analysis withcPandas & Seaborn

## DataScience Bootcamp Project 2 : WBS Coding School
This is my second data project! I will keep working on Eniac —the e-commerce tech company— as a Data Analyst. This time I will work with internal data, which is messy and unformatted. The complexity of these tasks will require me to use **Pandas**(a Python library) & **Seaborn**.

## Objective
To evaluate whether or not it’s beneficial to discount products.

# Main question

**Are discounts beneficial for the company?**

✅ The pros of discounts (according to the Marketing Team Lead) are :
- customer acquisition
- customer satisfaction
- customer retention
- allow the company to grow

❌ The cons of discounts (according to the main investors) are :
- recent quarterly results showed an increase in orders placed, but decrease in the total revenue
- positions the company in the quality segment, rather than competing to offer the lowest prices in the market

# Business questions

🗃️ Categories (introduced on 2024-05-17)
- How should products be classified into different categories to simplify reports and analysis?
- What is the distribution of product prices across different categories?

🚛 Discounts
- How many products are being discounted?
- How big are the offered discounts as a percentage of the product prices?

📅 Time period
- How do seasonality and special dates (Christmas, Black Friday) affect sales?

🌄 Outlook (recommendation at the end of the presentation)
- How could data collection be improved?
  Maybe it can be settled who is right and what needs to improve
    - Database Administrator, Khader, blames the buggy pipeline
    - Software Engineer, Lina, claims the issues have to do with wrong encodings and bad maintenance practices in our database
  
# Challenges :
- There are no customer data, so we cannot comment on customer satisfaction or retention
- Customer acquisition can be measured by the number of orders placed
- Company growth may be measured by the increase in orders placed
- The pros for discounts are based on long term benefits, so we need to assess the evolution of the entire period
- Unclear how to assess whether the company is more regarded as a discounter

# Analysis questions to get started (Keep asking questions)
- What is the time period that the dataset covers? (Priyanka)
- What is the overall revenue for that time? (Priyanka)
- Are there seasonal patterns in the evolution of sales? (Sören)
- What are the most sold products? (Sören)
- What are the products that generate the most revenue? (Muhammad)

# Data available
- `orders.csv` is useful for
    - time periods of orders
    - frequency of orders
    - trends of orders
    - total price paid for the order by the customer
- `orderlines.csv` is useful for
    - price paid of individual products (compared to the full retail price)
    - trends in product quantity
    - trends size of orders (how many products in one order)
    - trends in high or low price products over time and during discount periods
    - whether larger discounts are more popular than smaller discounts
- `products.csv` is useful for
    - calculating discounts
    - discounts by product categories
    - discounts by brands 
- `brands.csv` is not useful for the analysis but only used when visualizing the data with respect to the brand names

# Getting started
1. Decide on a cleaned dataset to use from now on
2. Discounts are defined as the difference between `orderlines.unit_price` and `products.price`.
   Merge both tables and create a column that contains the discount.
   Drop the columns that we don't need.

# Analysis for Presentation

- Discount by category (are some product categories more discounted than others), maybe also over the course of time? 
- Compare Jan/Feb 2018 to the months before Black Friday to see if the discounts "worked": Is there a substantial increase in orders/quantities/money per total order  
- Did Eniac lose revenue through discounts: Assess the current losses of the company by difference between actual revenue and revenue without discounts
  Compared to the increase in orders. Look for trends 
- Is Eniac becoming a discounter: What is the distribution of product categories in recent sales (and how it changed over time)? Are small appliances more popular than expensive products like computers and smartphones?
- *(Optional)* Customer satisfaction: difficult to assess, because there is no data like customer reviews (alternative: compare order state, e.g. how many have been completed versus cancelled or left in shopping cart)





