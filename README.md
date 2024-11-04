# Amazon_Vine_Analysis_ETL_Bias_in_PostgreSQL
This project involved performing an ETL process on an Amazon Review dataset, transforming it into four DataFrames, and loading them into PostgreSQL. It analyzed bias in Vine reviews by filtering data based on votes and helpfulness, calculating key metrics. The analysis was well-structured, addressing key questions and concluding on the presence of bias with recommendations.

## Overview
The purpose of this challenge was to analyze Amazon reviews written by members of the paid Amazon Vine program. I extracted a grocery dataset with reviews to specific products. I then utilized PySpark to extract and transform the dataset and connect to an AWS RDW instance. The transformed data was then loaded into pgAdmin. Pyspark allows us to determine if there exists any bias towards favorable reviews from vine members in our dataset  

Project Summary: Analysis of Amazon Product Reviews  

## Part 1: ETL Process on Amazon Product Reviews  
- Successfully extracted an Amazon Review dataset as a DataFrame.
- Transformed the dataset into four distinct DataFrames, ensuring all required columns were correctly aligned.
- Loaded all four DataFrames into their respective tables in pgAdmin for further analysis.

  
## Part 2: Bias Determination of Vine Reviews  
- Created a DataFrame/table for the vine_table data.
- Filtered the data to include entries with 20 or more total votes.
- Further refined the dataset to include entries where the percentage of helpful votes is 50% or higher.
- Segregated the data into two categories: Vine reviews and non-Vine reviews.
- Calculated key metrics: total number of votes, number of 5-star reviews, and the percentage of 5-star reviews for both categories.

  
## Part 3: Structure, Organization, and Formatting
- Developed a comprehensive written analysis featuring:
-  A clear title with multiple sections.
-  Well-defined headings and subheadings for each section.
-  Properly formatted images and code references to enhance clarity.

  
## Part 4: Analysis and Conclusions
- Clearly defined the purpose of the analysis.
- Addressed all three research questions in the results section.
- Concluded whether bias exists in the Vine reviews, supported by the analytical results, and provided an additional recommendation based on findings.

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
