# Amazon_Vine_Analysis

## Overview

The purpose of this project was to analyze Amazon Reviews to determine whether or not the paid review program Vine introduced a bias in the star rating of products. The Vine program either pays or sponsors individuals in exchange for a review on the product's Amazon page.

The scope of the analysis was limited to automotive products only. The dataset used can be imported from [this Amazon directory](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) under https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Automotive_v1_00.tsv.gz .

After the data was put through an ETL pipeline, Google Colab was used to turn it into usable dataframes which were in turn saved into a csv file. [The resulting file](https://github.com/MuzX9p088KKe/Amazon_Vine_Analysis/blob/main/Resources/vine_table.csv) was then further analyzed to answer the question central to this project: do paid Vine reviews create a bias in Amazon products star rating?

## Results

[The script used to analyze the reviews](https://github.com/MuzX9p088KKe/Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb) yielded the following results:

![Vine_reviews_results](https://user-images.githubusercontent.com/76575162/131230940-e7543416-48a2-47e3-a9ed-c7c84a343d0f.png)


### Paid Reviews
- There were 82 reviews which WERE a part of the Vine program.
-  This included 33 5-Stars reviews.
-  40.24% of the total were 5-Stars reviews.

### Unpaid Reviews
- There were 24742 reviews which were NOT a part of the Vine program. 
- This included 12807 5-Stars reviews
- 51.76% of the total were 5-Stars reviews.

## Conclusions

Although there is a difference of 11.5% of 5-star ratings between regular and vine reviews, it is worth noting that Vine reviews only account for .03% of total reviews. The sample size being this much smaller may have skewed the results for the paid reviews ratings. 

Further analysis is needed to get a better grasp of whether or not the Vine program causes a rating bias. Options include the following:
- Test all categories rather than only the automotive reviews.
- Check for bias among all other ratings as well rather than only 5-star reviews.
- Look at differences between the amount of Vine reviews across categories.
