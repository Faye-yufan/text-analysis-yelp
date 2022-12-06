# text-analysis-yelp
Becoming the Best Restaurant: Text Analysis Based on Yelp Reviews
Contributors: Aoxuan Ma, Linbo Chen, Tingxu Chen, Yixin Tao, Yufan Fei

## How to get the code to show the identical result?
- Download json files on [Yelp Dataset](https://www.yelp.com/dataset).
> Recommend using Jupyter Notebook in the following steps for better data visualization.
- Run _data-preparation/Read Review.ipynb_ **FIRST**.
- Run _01-EDA-and-Tokenize-Vectorization.ipynb_ in the root directory for EDA and vectorization process.
- Run _02-Clustering.ipynb_ to see unsupervised clustering results.
- After getting the clustering key words, we manually labeled the data in _Label sheets - Sheet1.csv_
- Run _03-Label-by-Classification-Models.ipynb_ for automatic labeling, generating _aspect_df.csv_ for the next step.
- Run _04-Regression-and-Feature-Importances.ipynb_ to see the importance and gain for each aspect.

## Problem Statement
Given a set of yelp rates and comment texts for restaurants collected on the yelp platform, we would like to determine the most representative features based on reviews and how they affect the rating scores for the restaurants. The results will let restaurant owners know their advantages and disadvantages and advise them to increase their chances of making profits.  

We will select people’s preferences of the restaurants, such as the flavor, service, or fame of restaurants, and find the relationship between the features and rating scores, whether there is a positive, neutral, or negative correlation between features and restaurants’ ratings, and interpret the reasons. Then we could help restaurant owners improve their restaurants to be more aligned with local preferences. According to the review text and rating score on Yelp, this is a possible chance to help local entrepreneurs make their restaurants more popular. 

## Data Source
- We use the official dataset on [Yelp Dataset](https://www.yelp.com/dataset).
- Some input .csv files were not uploaded on this repo due to the large file size, please download the zip file on [Yelp website](https://www.yelp.com/dataset), and put data files in the directory as _data-preparation/Read Review.ipynb_ shows.

## Conclusion and Future Work, and Lessons Learned
In terms of lessons, we have learned quite a few things in this project. In the process of clustering, we realized how closely related the keywords are in each cluster. We were able to confirm with the training scores in the classification model that these aspects exist objectively in the comments instead of some arbitrarily defined items. This experiment shows a lot of interesting possibilities to dive into the aspect selection process even more.

The results indicate just how important some specific aspects can be in predicting a customer’s rating of satisfaction. Specifically, food flavor is the most important one and service quality is the second. For future research and work, we can further split these 2 factors into more specific aspects. Since our 8 selected aspects derive loosely from our clustering results and were determined subjectively, we will be able to redo the aspect selection process to focus more on food flavor and service quality. For example, instead of just having a food flavor aspect, we can divide it into aspects such as food aesthetics, food quantity, food temperature, etc. By extending the most important aspects, we can recommend restaurants on more specific aspects to improve instead of just a loose recommendation on improving food and service.

Also, further prediction accuracy can be improved by other techniques such as advanced Sentiment Analysis and Entity Resolution. For the automatic labeling dataset, it is promising to combine the classifier with other Sentiment Analysis models such as BERT, which may have better performance in recognizing positive and negative emotions to improve the labeling accuracy. As for the aspect selection process, Entity Resolution can be applied here to get review clusters on different types of food flavors.

In conclusion, By analyzing over 640k Yelp reviews that users found very useful (>20 “useful”), we recommend restaurants put the most emphasis on their food flavor in an attempt to greatly improve their ratings. Although food flavor is the best predictor for user rating, we recommend restaurants also pay close attention to service quality, restaurant atmosphere (decor, hygiene, view, etc.), and price because they also play factors in predicting the rating.
