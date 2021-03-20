# Amazon_Vine_Analysis
Perform ETL on Amazon Product Reviews, determine Bias of Vine Reviews
This project analyzes Amazon Vine program and determines if there is a bias toward favorable reviews from Vine members.
The analysis uses PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin and calculate different metrics.
We focused on the US reviews for video games.

## Resources
Data Source: Amazon Review datasets, Video Games Review dataset
Software: Google Colab Notebook, PostgreSQL 11.9, pgAdmin 4, AWS

## Created 4 tables on pgAdmin4
1. Customers_table (customers_df)

![](Images/customers_table.PNG)

3. Products_table (products_df)

![](Images/products_table.PNG)

5. Review_id_table (review_id_df)

![](Images/review_id_table.PNG)

7. Vine_table (vine_df)

![](Images/vine_table.PNG)

## Results
### Total number of reviews
  - Vine reviews: 94 count
  
 ![](Images/number_paid_reviews.PNG)
  - Non-Vine reviews: 40,471 count
  
 ![](Images/number_unpaid_reviews.PNG)
  
### Total number of 5-star reviews
- 5-star Vine reviews: 48 count
![](Images/5star_paid_reviews.PNG)
- 5-star Non-Vine reviews: 15,663 count
![](Images/5star_unpaid_reviews.PNG)
### Percentage of 5-star reviews
  - % of 5-star Vine reviews: 51.06%
![](Images/percentage_paid_reviews.PNG)
  - % pof 5-star Non-Vine reviews: 38.70%
![](Images/percentage_unpaid_reviews.PNG)

## Summary
51% of the reviews in the Vine program were 5 stars reviews whereas the percentage in the non-Vine reviews is only 39%. This describes a positivity bias for reviews in the Vine program.
Additionally we could analyse the statistical distribution (mean, median and mode) of the star rating for the Vine and non-Vine reviews.
