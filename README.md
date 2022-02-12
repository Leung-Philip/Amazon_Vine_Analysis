# Amazon_Vine_Analysis

## Overview
An analysis was conducted on Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

One dataset from https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt was chosen for this analysis (pet products). Pyspark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Pandas was used for additional analysis on the Vine table that was created – determine if there is any bias toward favorable reviews from Vine members in the dataset. 

## Results
![Vine Analysis Table](Images/ vine_table_analysis.png)

- There were a total of 170 Vine reviews and 37,840 non-Vine reviews.
- There were a total of 65 Vine reviews that were 5-stars and 20,612 non-Vine Reviews that were 5-stars.
- The percentage of Vine reviews that were 5-stars was 38.24%. The percentage of non-Vine reviews that were 5-stars was 54.47%.


## Summary
There is no positivity bias for reviews in the Vine program for Amazon’s pet products category. Although there is a significant difference between the total of Vine reviews vs non-Vine reviews, there does not seem to be any positivity bias for reviews in the Vine program for Amazon’s pet products category since the percentage of Vine reviews that were 5-stars was 38.24% versus the percentage of non-Vine reviews that were 5-stars was 54.47%. 

Depending on how many stars is considered a good review, looking into 3-star and 4-star reviews may also help in determining whether there is any bias for reviews in the Vine program for Amazon’s pet products category. Furthermore, looking into 1-star and 2-star reviews may help in determining whether there is any negativity bias for reviews in the Vine program for Amazon’s pet products category.
