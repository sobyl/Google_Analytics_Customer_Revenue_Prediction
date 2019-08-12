# Dataset
[Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)

There are train and test dataset, and the mian features are:
- fullVisitorId- A unique identifier for each user of the Google Merchandise Store.
- channelGrouping - The channel via which the user came to the Store.
- date - The date on which the user visited the Store.
- device - The specifications for the device used to access the Store.
- geoNetwork - This section contains information about the geography of the user.
- socialEngagementType - Engagement type, either "Socially Engaged" or "Not Socially Engaged".
- totals - This section contains aggregate values across the session.
- trafficSource - This section contains information about the Traffic Source from which the session originated.
- visitId - An identifier for this session. This is part of the value usually stored as the _utmb cookie. This is only unique to the user. For a completely unique ID, you should use a combination of fullVisitorId and visitId.
- visitNumber - The session number for this user. If this is the first session, then this is set to 1.
- visitStartTime - The timestamp (expressed as POSIX time).
- hits - This row and nested fields are populated for any and all types of hits. Provides a record of all page visits.
- customDimensions - This section contains any user-level or session-level custom dimensions that are set for a session. This is a repeated field and has an entry for each dimension that is set.
- totals - This set of columns mostly includes high-level aggregate data.

The train data set collects view information of every Gstore customers and their cost from August 1st, 2016 to May 1st, 2018.

The test data set collects view information of every Gstore customers from December 1st, 2018 to January 31st, 2019, and the target is to predict how much they will spend on GStore during this period.

# Objective
This project will analyze a Google Merchandise Store (also known as GStore, where Google swag is sold) customer dataset to predict how much each customer will spend money on Gstore from December 1st, 2018 to January 31st, 2019.
As submission sample, using fullVisitorId as unique identifier for each customer and any other useful features to predict revenue per customer, which name as "transactionRevenue" in totals chunk.

# Motivation
The 80/20 rule has proven true for many businesses–only a small percentage of customers produce most of the revenue. As such, marketing teams are challenged to make appropriate investments in promotional strategies.

Online store analysis can educate the types of products customers like, customers distribution and many other useful factors. This can help make more educated decisions when it comes to product creation or curation for stores. I think this project may be more related to future work, and helpful accumulate realted experience.

# Challenges
The data set are really huge. The size of train data is 25.41GB with 12 colunms (if flatten all json columns, there will be more than 100 columns) and 1,708,337 rows. It will take a lot of time and memory to load and handle the data. The target value is unbalanced distribution, $98.9\%$ of them are NaN, and some of the rest are very larger.
