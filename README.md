# Dataset
[Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)

There are train and test dataset, and the mian features are:
- fullVisitorId- A unique identifier for each customer of the Gstore.
- channelGrouping - The channel via which the user came to the store.
- customDimensions - ???
- date - The date on which the user visited the Store.
- device - The specifications for the device used to access the Store.
- geoNetwork - This section contains information about the geography of the user.
- hits -  This section contains hits information.
- sessionId - A unique identifier for this visit to the store.
- socialEngagementType - Engagement type, either "Socially Engaged" or "Not Socially Engaged".
- totals - This section contains aggregate values across the session.
- trafficSource - This section contains information about the Traffic Source from which the session originated.
- visitId - An identifier for this session. This is part of the value usually stored as the \_utmb cookie. This is only unique to the user. For a completely unique ID, you should use a combination of fullVisitorId and visitId.
- visitNumber - The session number for this user. If this is the first session, then this is set to 1.
- visitStartTime - The timestamp (expressed as POSIX time).

# Objective
This project will analyze a Google Merchandise Store (also known as GStore, where Google swag is sold) customer dataset to predict revenue per customer. As submission sample, using fullVisitorId as unique identifier for each customer and any other useful features to predict revenue per customer, which name as "transactionRevenue" in totals chunk.

# Motivation
The 80/20 rule has proven true for many businesses–only a small percentage of customers produce most of the revenue. As such, marketing teams are challenged to make appropriate investments in promotional strategies.

Online store analysis can educate the types of products customers like, customers distribution and many other useful factors. This can help make more educated decisions when it comes to product creation or curation for stores. I think this project may be more related to future work, and helpful accumulate realted experience.

# Challenges
The data is really huge. The size of train data is 25.41GB with 60+ colunms and 903,653 rows. It will take a lot of time to load and handle the data, much more time to build the model. And there are some of the fields looks like json, but not, and need to convert to a flattened csv format for further analyse.
