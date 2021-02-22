# Amazon Vine Analysis
  Analysis of Amazon Rating Review Bias
  
## Overview of the analysis
Determine if there is any bias towards reviews that were written as part of the Vine program. For this analysis, we will determine if having a paid Vine review makes a difference in the percentage of 5-star reviews.
  
## Resources
- Data Source: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz, AWS RBS
- Software: PySpark, Pandas, PostgresSQL, pgAdmin4, Jupyter Notebook, VSCode

## Results
Analysing Video Games reviews in the US, we got the following results:

  - Total Qualified* Reviews:
    - Vine:     102
    - non-Vine: 64,008

  - Total 5 Stars Qualified* Reviews:
    - Vine:     48
    - non-Vine: 20,282

  - Percentage of 5 Stars / Total:
    - Vine:     47.06%
    - non-Vine: 31.69%

  *Qualified is defined as having total votes equal to or greater than 20 and helpful votes over total votes equal to or greater than 50%, as shown in the Dataframes below"
  
  - Total Voters equal to or greater than 20

   ![top_votes](/top_votes.png)

  - Helpful votes over total votes equal to or greater than 50%

  ![helpful](/helpful.png)
  
  - Part of the Vine Program (paid)

  ![paid](/paid.png)
  
  - Not part of the Vine program (unpaid)

  ![unpaid](/unpaid.png)
  
- Result Output

![VG_reviews](/VG_reviews.png)
  
## Summary

Looking at the results, we can conclude that there is in fact a positivity bias for reviews in the Vine program (47.06% against 31.69% non-Vine reviews).  A possible reason is the fact that unpaid reviewers tend to be more critic, while participants tend to be more constructive.

One additional analysis that could be done with the dataset is using machine learnimg validate the rating against the written reviews, and get more insight from the these reviews.
