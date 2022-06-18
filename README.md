# Amazon_Vine_Analysis

## Overview of Analysis:

The purpose of this analysis is to analyze Amazon reviews written by members of the paid Amazon vine program. The vine program is a service that allows manufacturers and publishers to receive reviews for their products. Some companies will pay a fee to Amazon and provide products to Amazon vine members, who are then required to publish a review. 

I decided to pick the dataset on shoes for review. I used PySpark to perform the ETL process to extract and transform data, connect to AWS RDS instance, and load the transformed data into pgAdmin. I then used PySpark to determine if there is any bias towards favorable reviews from vine members in this dataset.  

## Results:

Below are the four different tables that were created in pgAdmin from the shoe dataset. I then I took the vine-table and performed and analysis to determine if there was any bias between vine reviewers and ratings. 

Customers Table: 

<img width="250" alt="pgAdmin-customers_table" src="https://user-images.githubusercontent.com/100392991/174421924-488cc931-869a-46af-81e6-f370533f7959.PNG">

Products Table:

<img width="600" alt="pgAdmin-products_table" src="https://user-images.githubusercontent.com/100392991/174421962-84a36a1e-aa77-4567-9e2f-e83bed79b75a.PNG">

Review ID Table:

<img width="430" alt="pgAdmin-review_id_table" src="https://user-images.githubusercontent.com/100392991/174421983-71c3f4f1-3255-491f-b571-0e7504e3d68c.PNG">

Vine Table:

<img width="450" alt="pgAdmin-vine_table" src="https://user-images.githubusercontent.com/100392991/174421992-120baedb-c4c9-4338-a073-c8ad6b4b97b9.PNG">


1. How many Vine reviews and non-Vine reviews were there?
  - There are a total of 22 vine reviews in the shoe dataset and 26,987 non-vine reviews.

2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
  - There were 13 5-star reviews from vine reviewers in the shoe dataset and 14,475 5-star reviews from non-vine reviewers.

3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
  - 59.09% of all vine reviewers gave 5-stars and 53.64% of all non-vine reviewers gave 5-stars in this shoe dataset. 


## Summary:
1. Are there any positivity bias for reviews in the Vine program? Support your statement.
  - I would say there is not any positive bias for reviews in the vine program. Both the vine reviewers and non-vine reviewers had similar 5-star ratings: 59% for vine members and 54% for non-vine members. Actually, there are A LOT more reviews and 5-star reviews from non-vine members so I would take this dataset to be fairly bias free seeing as there are so many positive reviews from non-vine (unpaid) reviewers.

2. What is one additional analysis that you could do with the dataset to support your statement?
  - We could perform the same analysis but with 1-star reviews to see if there are any bias with negative reviews. We could also analyze the number of helpful votes with vine and non-vine members to see if that tends to generate a pattern or any bias in the reviewers. 


