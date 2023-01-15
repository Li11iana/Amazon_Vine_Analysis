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

* A total of 14477 reviews were written by regular customers, not part of the Vine program.
* The number of reviews made by regular customers far supersedes those made by Vine members.
* There were reviews were classified as follows:
  * 1-star = 1532 reviews 
  * 2-star = 754 reviews 
  * 3-star = 1292 reviews
  * 4-star = 2687 reviews
  * 5-star = 8212 reviews
* The percentage of 5-star reviews matches with the Vine members table, with 56.72% of the total reviews analyzed in this dataframe. 

![Normal_reviews](https://github.com/Li11iana/Amazon_Vine_Analysis/blob/main/Normal_reviews.png)


# Summary:

Reviewing the data provided it appears clearly that there is a significative difference between the number of reviews by Vine members compared to those by regular non-Vine customers, this difficults the comparison specially in a category like "Musical Instruments" that does not have the level of traffic as other Amazon shopping categories.
However, when comparing the two dataframes generated we can conclude:
* The percentage of 5-star reviews remains consistent between the two groups, Vine members 56.66% and non-Vine customers 56.72%. We can infer that the Vine members are not grading the products with easier to lower standards than the average online shopper, therefore to the extent of this analysis there is no evidence of bias from the Vine members.
* Where 10.58% of the reviews made by non-vine member qualified the product with 1-star, there were zero 1-star reviews from the Vine-members. 1-star reviews label truly bad products, poor quality items, unpleasant customer service, and overall disagreeable experience for the customer.
Instead of marking this as a potential evidence of bias from the Vine reviewers, this could be explained as vendors part of the Vine program would  likely be more interested in improving their sales and consequently with providing a better experience for the customer 

### Additional analysis
To improve the insights provided by the data, I would be beneficial to review cases of products with numerous reviews from both Vine and non-vine customers, this could show more clearly if there is bias from the program.
Good reviews are a key to more purchases, often considering a deciding purchasing factor on Amazon. As an additional insight for the vendors an analysis per product or vendor showing the date and number of reviews writen could prove if being part of the Vine program increases the popularity of the items.
