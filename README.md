# Data-Cleaning & Analysis withcPandas & Seaborn

## DataScience Bootcamp Project 2 : WBS Coding School
This is my second data project! I will keep working on Eniac —the e-commerce tech company— as a Data Analyst. This time I will work with internal data, which is messy and unformatted. The complexity of these tasks will require me to use **Pandas**(a Python library) & **Seaborn**.

## Objective
To evaluate whether or not it’s beneficial to discount products.

## Skills & Tools :
- Data Cleaning & Quality Assurance
- Data Visualization & Storytelling
- Colab & Jupyter Notebook
- Python: Pandas, Seaborn, Matplotlib

## Project Contributors:
Group of 3 peoples contributed in this project work.

## Main question

**Are discounts beneficial for the company?**

✅ The pros of discounts (according to the Marketing Team Lead) are :
- customer acquisition
- customer satisfaction
- customer retention
- allow the company to grow

❌ The cons of discounts (according to the main investors) are :
- recent quarterly results showed an increase in orders placed, but decrease in the total revenue
- positions the company in the quality segment, rather than competing to offer the lowest prices in the market

## Business questions

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
  
## Challenges :
- There are no customer data, so we cannot comment on customer satisfaction or retention.
- Customer acquisition can be measured by the number of orders placed.
- Company growth may be measured by the increase in orders placed.
- The pros for discounts are based on long term benefits, so we need to assess the evolution of the entire period.
- Unclear how to assess whether the company is more regarded as a discounter.

## Analysis questions to get started (Keep asking questions)
- What is the time period that the dataset covers? (Priyanka)
- What is the overall revenue for that time? (Priyanka)
- Are there seasonal patterns in the evolution of sales? (Sören)
- What are the most sold products? (Sören)
- What are the products that generate the most revenue? (Muhammad)

## Data available
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

## Data Cleaning
The dataset underwent a rigorous cleaning process to ensure data integrity:

**Corrupted Database:** Identified and addressed issues that affected the overall integrity of the database.
**Incongruent Data:** Resolved inconsistencies, mismatched, and/or duplicate data.
**Double Dots Numbers:** Rectified anomalies in numerical values, focusing on duplicated or irregular decimal points.
**Data Quality Concerns:** Mitigated issues affecting the reliability and completeness of the dataset.


## Getting started
1. Decide on a cleaned dataset to use from now on
2. Discounts are defined as the difference between `orderlines.unit_price` and `products.price`.
   Merge both tables and create a column that contains the discount.
   Drop the columns that we don't need.

## Analysis for Presentation

- Discount by category (are some product categories more discounted than others), maybe also over the course of time? 
- Compare Jan/Feb 2018 to the months before Black Friday to see if the discounts "worked": Is there a substantial increase in orders/quantities/money per total order  
- Did Eniac lose revenue through discounts: Assess the current losses of the company by difference between actual revenue and revenue without discounts
  Compared to the increase in orders. Look for trends 
- Is Eniac becoming a discounter: What is the distribution of product categories in recent sales (and how it changed over time)? Are small appliances more popular than expensive products like computers and smartphones?
- *(Optional)* Customer satisfaction: difficult to assess, because there is no data like customer reviews (alternative: compare order state, e.g. how many have been completed versus cancelled or left in shopping cart)

## Datasets :
- `order_qu.csv` - quality controlled
- `orderlines_qu.csv` - quality controlled
- `products_cl.csv` - cleaned
- `brands.csv` - original
- `categories.csv` - newly created

**Note** These files are available in the folders created in this repository.

## Colab Files :
1. [Data Cleaning](https://colab.research.google.com/drive/1aekiUw5vvjATC5m_uNIjuuhWc21kRg5i?usp=sharing)
2. [Data Quality Assessment](https://colab.research.google.com/drive/1MgN8IDyB5M4i32cgYjQSSsLEkPEV87p2?usp=sharing)
3. [Category Creation(Decided in a group)](https://colab.research.google.com/drive/13InWevrxR1wkZf08V0vD5x2pTJ7f9X92?usp=sharing)
4. [Final Data Analysi(My Task)](https://colab.research.google.com/drive/1aekiUw5vvjATC5m_uNIjuuhWc21kRg5i?usp=sharing)


## Recommendation for data management

● Database Administrator, Khader, should fix currency encodings (commas and periods).
● Software Engineer, Lina, should provide consistent currency formats.
● Create a documentation of the database for the future.
● Add customer reviews to database to allow analysis of customer satisfaction

## Conclusion

- Discounts have been beneficial
- 1. Lower price products are discounted more than expensive products.
  2. Customer behavior is stable over time.
  3. Sales increased compared to the previous spring.
     
Limit discounts to special occasions, reduce discount on high-price products.

## Some Snapshots of this Project :

![Loss of revenue through discounts is small](https://github.com/PriyankaSPawar/Data-Cleaning-and-Storytelling_with_Pandas_Seaborn/assets/168557945/d6d9fee2-e58a-43f1-b94f-b8db3d817be2)
![Lower price products are discounted more](https://github.com/PriyankaSPawar/Data-Cleaning-and-Storytelling_with_Pandas_Seaborn/assets/168557945/5f316fbf-958b-4b76-a918-43fb802fd3ec)
![Revenue increased despite discounts](https://github.com/PriyankaSPawar/Data-Cleaning-and-Storytelling_with_Pandas_Seaborn/assets/168557945/d565e3da-6d18-46e0-9615-c392c6e3dc24)
![image](https://github.com/PriyankaSPawar/Data-Cleaning-and-Storytelling_with_Pandas_Seaborn/assets/168557945/8a64f156-82c6-4ed2-aac8-e8c1cb7f0547)
![Product Categories Analyzed](https://github.com/PriyankaSPawar/Data-Cleaning-and-Storytelling_with_Pandas_Seaborn/assets/168557945/7f075658-284e-4873-bb9d-2591d4ad26d3)
![Difference in discount rate between 2017 and 2018](https://github.com/PriyankaSPawar/Data-Cleaning-and-Storytelling_with_Pandas_Seaborn/assets/168557945/03362ce1-9e6f-4844-b30a-67fe620a5198)








