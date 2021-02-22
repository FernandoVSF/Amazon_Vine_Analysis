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
  
  
  

  

  - Initial Page
  
![initial](/initial.png)

   - Filtering by Shape = light
  
![f1](/f1_shape.png)
  
   - Adding filter by State = ca
  
![f2](/f2_state.png)

   - Adding filter by City = el cajon
  
![f3](/f3_city.png)

   - Adding filter by Date = 1/1/2010
  
![f4](/f4_date.png)
 
## Summary

One drawback of this design is that it requires the user to scroll over the whole list to select the input for the search criteria.  Another one is not being possible to reset filters (although we can select a new criteria for the filter).

As a recomendation for further dvelopments, I suggest the following:

  - Implementing combo boxes in the input fields, to show the possible selections and avoiding typos;
  
  - Implementing an option to reset filters, by "showing all" in the combo box suggested above.
  
