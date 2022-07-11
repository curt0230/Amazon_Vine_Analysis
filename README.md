# Amazon_Vine_Analysis
## Project overview
The purpose of this project was to perform an analysis of Amazon Vine reviews to determine if the program, which pays or provides members with free products that they must in turn write reviews for.  Out of 50 product-specific data sets, this analysis focused on approximately 5 million reviews of pet supplies.


## Resources
* Software:  Apache Spark 3.0.3, PostgreSQL on AWS, S3, Google CoLaboratory
* Data sources:  
  * https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz

## Analysis
Amazon rating data collected to perform this analysis.  This data was cleansed, aggregated, and tranformed using PySpark via Google CoLab into a unified schema and loaded into a PostgreSQL cloud database on AWS.  It was also filtered and aggregated, again using PySpark in Google CoLab to create summary statistics.

## Results
Using bulleted lists and images of DataFrames as support, address the following questions:

![summary.png](/summary.png)

Here are some key points:
* In total, 5,125,423 reviews were studied.  Of those, 23,943 were associated with Vine customers.
* Of the 23,943 Vine reviews, 8,699 were five-star reviews.
* Of the remaining 5,101,480 reviews, 2,686,517 were five-star reviews.
* Approximately 52.59% of non-Vine reviews were five-star reviews, and only 36.33% of Vine reviews were five-star reviews.

## Summary
In short, there appears to be a negative relationship where Vine reviewers are less likely to give a five-star review than the general population of customers.  There could be multiple reasons for this.  People might wish to appear less biased because of the known relationship with the retailer, the products that are being promoted may have quality issues, or the reviewers may have other motives for writing better or worse reviews.

An additional analysis is recommended to study and categorize sentiment in reviews to see how it correlates with the star rating.  This investigation could focus on whether neutral reviews tend to be positive or negative in sentiment, and whether that impacts the overall result.
