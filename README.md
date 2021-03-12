# News popularity analysis and prediction

With the expansion of the Internet, more and more people enjoys reading and sharing online news articles. The number of shares under a news article indicates how popular the news is. In this project, I intend to find the best model and set of feature to predict the popularity of online news, using machine learning techniques.

## Data 

The dataset is from UCI machine learning repository, and I attach the link here https://archive.ics.uci.edu/ml/datasets/online+news+popularity. There are 39644 rows, 61 columns and the last column share is my target variable. 

## Analytic goals
I plan to first decide the threshold and convert it to 2 classes, which would be popular and not popular, so my project is actually a binary classification problem. The analytic goals include:

1. Convert the target variable to binary format.
2. Preprocess the data appropriately.
3. Fit model for binary classification and check the performance.
4. Find the best model with grid search and randomized search.
5. Make conclusions.

## Takeaways

Here I would like to make further explanation on some key points of my project.

1. Why I use 2/3 of training data to perform grid search?

Since I still do randomized search in later steps, so the goal of grid search is to have a general idea about these models' performance. 


2. The best based on all search methods is Random Forest. So why it would be the best model?

I am not surperised that Random Forest performs the best, since:

Compared with Logistic, Linear SVC, LGBMClassifier, Random Forest use the ensemble method which composed of multiple trees and use majority vote to make final decision. The magic of improved performance is often the reduction in the variance of predicted errors made by its contributing models.

Compared with ExtraTreeClassifier, Random Forest use bootstrap replica but ExtraTree use the original whole data, so ExtraTree may get higher variance. Besides, Random Forest choose best split to minimize loss while ExtraTree use random value. Therefore ExtraTree add randomization.


3. Why this topic is important?

In the recent decades, online news became a new popular source for people to obtain news, and for most of the times, people would only focus on the hot topics. Also, reading and sharing news have become the center of people’s entertainment lives. If we could predict the popularity of news prior to its publication, it would be valuable for social media companies, also some authors and advertisers. They can have a prior understanding on what kind of news will receive more clicks, then they can make certain changes on the news' content to make it more popular.



