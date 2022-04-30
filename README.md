# Amazon_Vine_Analysis

## Overview

In this project the main task was to extract data from amazon s3 servers, transform it using pyspark and then uploading the cleaned data to a SQL database, hosted in the cloud thanks to AWS. After the data was stored, an analysis was made to determine if paid reviews are skewed toward a positive opinion or is it the same as non paid review. For this project, the "video-game" data set was selected which contained information of all video game related items in amazon.

In this project I learned to use AWS to host databases and files. Not only was I able to use this technology, I also learned the value of it and how we can benefit by using it.

## Results

### SQL database

The first outcome of this project is a database containing 4 different tables that relate to each other. We can see this tables in the images below.

![customers SQL](https://user-images.githubusercontent.com/95836718/165822258-440e9460-21e1-4b10-925a-11bd0ee129b8.png)

***Comment:*** *This table contains all the customer id and how many purchases they have.*

![Products_SQL](https://user-images.githubusercontent.com/95836718/165822461-e2945ef6-68b8-412b-af0e-c0b15e52c6ba.png)

***Comment:*** *This table contains all the products id and its title to see all the products available for reviews.*

![Review_id_SQL](https://user-images.githubusercontent.com/95836718/165822570-db0e7637-316b-4c72-9311-210121b02f4f.png)

***Comment:*** *In this table we can see each individual review and the product it is adressing.*

![vine_SQL](https://user-images.githubusercontent.com/95836718/165822738-4915f21c-1ba6-4a80-918f-37ea99898b23.png)

***Comment:*** *This table contains the information needed to understand and analyze if there is any inclination towards a more positive review if the review was paid for.*

### Paid and Unpaid reviews analysis

After filtering the results for those that had more than 20 votes and that theyre helpful votes represented more than 50% of their total votes, we got the next results.

- We have a total of 94 paid reviews and 40471 unpaid reviews
- There is total 5-star reviews of 48 paid reviews and 15663 unpaid reviews.
- This reviews acount for  51.06% paid reviews and 38.7% reviews.

The following images splits this information in paid and unpaid reviews.

![paid_results](https://user-images.githubusercontent.com/95836718/165825077-989d1cd5-f73b-4ecc-b8b4-bcafd381dce1.png)

***Comment:*** *Paid Reviews*

![unpaid_results](https://user-images.githubusercontent.com/95836718/165825141-2b09431a-7b90-4585-8330-6b27f4a64fc1.png)

***Comment:*** *UnPaid Reviews*

## Summary

Looking at the results we can see that, in percentage, there are more 5-star votes in the paid reviews than in the unpaid reviews. There is a difference of 12.6% points. Although this may represent a trend towards more positive reviews, we can not jump into conclusions yet. In order to gather more insight we can do this same analysis but for 4-star, 3-star,2-star and 1-star reviews. With this we can see more clearly if there is any preference, or maybe they are more drastic and paid reviews choose only 5s or 1s.
