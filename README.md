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


