# Mobile-App-Analysis
EDA and analysis of dataset google-play-store-apps from kaggle

Author: Xinrui(Cindy) Chen

This a final project report for course Data Science I.The report can be viewed [Here](https://www.kaggle.com/chenxinrui/eda-and-analysis)

## Abstract

 Considering the fastest growing of mobile app market, the app data has enormous potential to drive app-making businesses to success. In this study, I explored the performances of apps to provide a guidance for app development. To be specific, biplot was used to evaluate performances of apps in different categories in price, rating and installs, the factors related to rating were shown in visualization and finally all apps were clustered into 10 smaller groups through k-prototypes clustering after dimensionality reduction by PCA. 
 Key words: Clustering, PCA, k-prototypes, biplot, Visualization
 
 
## Introduction and Background

 Mobile applications have been a part of smartphones for over a decade. Mobile App Market is the fastest growing segment in the mobile industry. Customers, developers and distribution platforms all benefit from mobile app industry. Therefore, it is very meaningful to analyze mobile app market in order to track for the success of apps. Google Play and the Apple App Store are the leading distribution platforms for mobile applications, and our data derives from Google Play Store. In the main dataset, over 10,000 apps are included and each app has values for its own category, rating, size, price, content rating, number of installs, number of ratings and genres. To further explore the reviews, I had external dataset containing sentiment (positive or negative), polarity and subjectivity grade of sentiment in each review for all the apps. These data were scraped from Google Play Store 10 months ago. 
  In this study, I mainly focused on three questions:(1) How about the performances of apps in different categories regarding ratings, prices and installs? (2) How do different variables influence the rating of apps? (3) How to cluster apps into a specific number of clusters? By answering these questions, from a developer's perspective, we can better decide which category of apps should we develop and have a clear idea of how to make a high rating app, and we can further explore similar apps in the same cluster as the apps we are interested in.
  
  
## Methods

 (1) Data cleaning: 
 The data was cleaned through removing duplicate records and errors in the data like redundant symbols, transforming the data type and dealing with missing values. 
 (2) Libraries used: 
 The libraries pandas, numpy, matplotlib, seaborn, kmodes and sklearn were used. 
 (3) Questions: 
 For question one, I focused on three variables, namely ratings, installs and prices since they are the most important indicators for developers. We desire a better rating, the most installs and a relatively better price to earn money. I dismissed reviews and other variables since they are not the top priorities for consideration when developing an app. Therefore I calculated the average ratings, installs and prices for each category of apps and then I extracted two principle components using PCA in order to better visualize them. Finally, I drew a biplot and we can evaluate performances of apps in different categories. 
 For question two, I visualized the relationships between prices, installs, reviews, content ratings and ratings separately. Then we can analyzed their inner associations. 
 For question three, in order to cluster the apps into smaller groups, I considered as many variables as possible, that are ratings, reviews, installs, prices, category and content rating. I merged the external data with main dataset in order to take reviews into consideration since the number of reviews alone doesn't tell the story. We also need to know the sentiment of the comments. Considering the inner correlation within review-related variables, I first performed PCA on all the continuous variables. Then considering we have both continuous and categorical variables at the same time, I used k-prototypes clustering.Finally I visualized each app stratified by its cluster and we can obtain the cluster for each app.



