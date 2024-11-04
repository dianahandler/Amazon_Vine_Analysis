## Overview
The purpose of this challenge was to analyze Amazon reviews written by members of the paid Amazon Vine program. I extracted a grocery dataset with reviews to specific products. I then utilized PySpark to extract and transform the dataset and connect to an AWS RDW instance. The transformed data was then loaded into pgAdmin. Pyspark allows us to determine if there exists any bias towards favorable reviews from vine members in our dataset  

## Results
* How many vine reviews and non-vine reviews were there?
  There were a total of 28,235 reviews
  Vine reviews: 61
  Non-vine reviews: 28,174
    
* How many vine reviews were five stars? 
  There were a total of 20 5-star vine reviews
  
* How many non-vine reviews were five stars?
  There were a total of 15,672 non-vine 5-star reviews
  
* What percentage of vine reviews were five stars?
  Approximately 33% of vine reviews were 5 stars

* What percentage of non-vine reviews were five stars?
  Approximately 56% of non-vine reviews were five stars

![vine_results](https://user-images.githubusercontent.com/82029390/128649962-757b94f3-9328-4f2e-a95f-7a3c5f9722fd.png)



## Summary
It is highly unlikely that there is any positivity bias with this dataset. Out of a total of 28,235 reviews, only 61% of those were vine reviews. Furthermore, only 1/3 of those vine reviews were 5 stars. The vast majority of reviews come from unpaid members with 15,672 non-vine 5 star reviews. It would be additionally helpful to analyze the paid vine reviewers' review history to assess whether they have a history of reviewing other products from other companies or if they only reviewed this particular item, suggesting paid bot usage. 
