# text-analysis-yelp
Becoming the Best Restaurant: Text Analysis Based on Yelp Reviews

## How to run the code?
- Download json files on [Yelp Dataset](https://www.yelp.com/dataset).
> Recommend using Jupyter Notebook in the following steps for better data visualization.
- Run _data-preparation/Read Review.ipynb_ **FIRST**.
- Run the _ipynb_ files in the root directory.

## Problem Statement
Given a set of yelp rates and comment texts for restaurants collected on the yelp platform, we would like to determine the most representative features based on reviews and how they affect the rating scores for the restaurants. The results will let restaurant owners know their advantages and disadvantages and advise them to increase their chances of making profits.  

We will select people’s preferences of the restaurants, such as the flavor, service, or fame of restaurants, and find the relationship between the features and rating scores, whether there is a positive, neutral, or negative correlation between features and restaurants’ ratings, and interpret the reasons. Then we could help restaurant owners improve their restaurants to be more aligned with local preferences. According to the review text and rating score on Yelp, this is a possible chance to help local entrepreneurs make their restaurants more popular. 

## Dataset
- We use the official dataset on [Yelp Dataset](https://www.yelp.com/dataset).
- Some input .csv files were not uploaded on this repo, please download the zip file on [Yelp website](https://www.yelp.com/dataset) **BEFORE** run the _data-preparation/Read Review.ipynb_.
- Execute _data-preparation/Read Review.ipynb_ to generate _yelp_review.csv_ **BEFORE** run the _yelp_review_best_team.ipynb_.
