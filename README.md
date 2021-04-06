# Project Overview
The goal of the project is to predict the price of a Laptop, if given the specifications for it. 
* Built a model that estimates the price of laptop for the required brand and specification
* Scrapped the required data to build a model from Amazon and built a dataset with aproximately 2700 records.
* Cleaned the data by removing duplicate records and irrelevant data.
* Created new features from the cleaned data.
* Built a model and tuned it for better results.

# Code and Resources Used
* Python Version: 3.9
* Packages: pandas, numpy, sklearn, matplotlib, seaborn, beautifulsoup, Selenium.
* Data scrapped from *Amazon*.

# Web Scrapping
Built a web scrapper from scratch which is specifically built for this. It scrapped all the details availabe in the index page of each product. It iterated over *400 pages* to collect roughly *2770 records*. The gathered data includes,
* Title/Description
* Rating
* Number of Reviews
* Storage type
* Display size
* CPU Speed
* RAM

# Data Cleaning
As the Amazon website contained many repeated sponsored ads for laptop and some irrelavant contents as moving across the pages, it required lot of cleaning.
* Dropped all the Duplicate records.
* Filtered records which are not laptops.
* Removed extra symbols like £ etc..
* Changed the data type to relavant ones.

# Feature Engineering
Since I just scanned the index page, it did not contain all the details.
* Created new features from title such as,
  * OS
  * Graphics card
  * Brand
* Created a new column for Ratings per user.
* Created a new feature named Processor type from Title.

After performing cleaning and engineering we ended up with only roughly *600 records of data*.

# Exploratory Data Analysis
### Count Plot for brands
The first thing I did was to look at the countplot to see the spread of data across brands. It is obvious that there are many laptops labels as *Other brand* because of the lack of proper title or might be too small to give a seperate column for.


![count plot](https://github.com/ArunGautham-Soundarrajan/Laptops_Price_Predictor/blob/main/images/countplot_brand.png)

### Number of Reviews
As amazon doesnt provide details of how many times a product have been purchased, we can't find the popular brand or most go to brand. But still we can consider *Number of reviews* as an alternative to it.

![number of reviews](https://github.com/ArunGautham-Soundarrajan/Laptops_Price_Predictor/blob/main/images/reviews_for_each_brand.png)

From the plot, we can clearly see *Asus* got second most number of reviews as I can't take *other brands* into context, even I owned an ASUS Laptop before, I though it was great for the price. Moving on, it seems like *Dell* is least favourite across these brands, may be they should work on advertising more.

### Average price for Each Brand

![avg price](https://github.com/ArunGautham-Soundarrajan/Laptops_Price_Predictor/blob/main/images/avg_price_brand.png)

* As we all know, *Apple* laptops are more expensive and surprisingly *Dell* is the second most expensive brand, may be that's why people did'nt go for it.
* *Asus, HP and Other brand* have higher sales and looking this plot shows why, cause they are available at a very reasonable price. 
* I wonder why *Lenovo* did'nt go that well considering the price, may be there might be other factors to consider.

### Average Ratings for Each Brand

![avg_rating](https://github.com/ArunGautham-Soundarrajan/Laptops_Price_Predictor/blob/main/images/avg_rating_brand.png)

From the plot,
* *Acer* has the highest rating and it's price is pretty standard. But still it managed to get only *8500* reviews roughly.
* *Apple* has second highest rating with an average of 4.35 Stars out of 5. They might be worth every penny.
* We can also see that, all the averages are above 4, so I should consider scrapping the data more accurately, so we can get better insights from it.

It does'nt mean that, there are no laptops with rating below 4 stars, we can take a look at Distribution of ratings to get better insight.

![Rating Dist](https://github.com/ArunGautham-Soundarrajan/Laptops_Price_Predictor/blob/main/images/rating_dist.png)
* *Asus* got 1 star rating for one or two latops may be, my bad.
* Other brand latops also got ratings less than 3.
* But I can clearly see, *Asus , Dell and Other brand* laptops have many reviews less than three. Which might indicate, we want to double check before consider buying one.

These are some of the useful explorations to note one, while there are still more.


