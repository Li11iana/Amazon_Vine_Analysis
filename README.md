# Amazon_Vine_Analysis
Big Data Analysis of customers reviews using AWS and PostgreSQL for Amazons marketplace "Musical Instrument" cathegory.

# Overview of the analysis:
For this challenge, the Amazon Vine Program will be analyzed for a specific product cathegory. 
Companies looking to appeal to Amazon consumers pay a fee to have their products be reviewed by Amazon Vine members who promise reliable and interesting product commentary.
Data analysis will be conducted using PySpark in synchrony to Amazon AWS database and S3 services.

## Objective
Provide a big data analysis synthesizing the key differences between reviews written by Vine members and regular customers for the Amazon's "Musical Instruments' cathegory. 

# Results: 

The dataset evaluated on this project correspond to product reviews of items withing the "Musical Instruments" cathegory sold on Amazon.com and was retrieved from the following URL:

* https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Musical_Instruments_v1_00.tsv.gz

Dataset was extracted using pgAdmin to generate the required schemas.Groupped and filtered tables were exported and uploaded to S3 to facilitate further inspection. The reviews with less than 20 interactions (votes indicating if the review was helpful or not) where dropped and would not be included in the rest of the analysis.
Finally two additional dataframes were generated to contrast the statistics of the reviews created by Vine program member versus the reviews written by regular customers.

### Vine program members

* A total of 60 reviews were written by Vine members.
* There were no 1-star reviews
* There was only one entry given 2-stars, nine entries corresponded to 3-star reviews, sixteen 4-star reviews and thirty-four 5-star reviews.
* Over half of the reviews correspond to 5-star reviews (56.66% of the total reviews by Vine members).


![Vine_reviews](https://github.com/Li11iana/Amazon_Vine_Analysis/blob/main/Vine_reviews.png)

### Regular customers

* A total of 60 reviews were written by Vine members.
* There were no 1-star reviews
* There was only one entry given 2-stars, nine entries corresponded to 3-star reviews, sixteen 4-star reviews and thirty-four 5-star reviews.
* Over half of the reviews correspond to 5-star reviews (56.66% of the total reviews by Vine members).
![Normal_reviews](https://github.com/Li11iana/Amazon_Vine_Analysis/blob/main/Normal_reviews.png)

* Vine members

* How many Vine reviews and non-Vine reviews were there?
How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
!https://github.com/Li11iana/Amazon_Vine_Analysis/blob/main/Normal_reviews.png

# Summary:
In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one ad
