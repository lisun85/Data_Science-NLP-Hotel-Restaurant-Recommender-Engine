# Hotel & Restaurant – Natural Language Processing

The goal of this project is to use natural language processing (NLP) algorithms to: 1. construct Topic Modeling, 2. Conduct Sentiment Analysis, 3) and build a Recommender Engine for Hotels and Restaurants on TripAdvisor and Zomato. Working with hotel and restaurant review data, I used Non-negative Matrix Factorization to conduct my topic modeling. I used VADER to conduct sentiment analysis, and I TF-IDFI with Cosign-Similarity Matrix to build the Recommender Engine.

Design

Hotels and restaurants are service-oriented industries that proves to be very competitive. The one element that significantly impacts the industry is user reviews. Positive reviews written on websites like Trip Advisor or Zomato will lead to more business, while negative reviews can severely damage the hotel or restaurant’s reputation. Reviews gathered from hotels and restaurants are rich datasets that if mined and analyzed correctly can yield important business insights. So, the problem we are trying to solve today is: 
1. From the hotel reviews, how do find main topics among all reviews + how positive or negative are the reviews? 
2. From the restaurant reviews, how do we build a recommender engine so that users can pick similar restaurants. 


Data

Data is pulled directly from Kaggle. There are two datasets. First data set is hotel reviews from Trip Advisor. The data contain two features (Free-Form Text Reviews and Ratings) with each row representing a hotel (20k+ total rows). The second data set is restaurant reviews from Zomato with 10 features (url, address, name, rating, location, etc.). Each row represents a restaurant and there are 40k+ total rows.

Algorithms

Topic Modeling:

	Count-Vectorizer with LSA – Topics were not that well defined even after tuning

	TF-IDF with NMF – After several tuning, 4 topics surfaced and are well defined

Sentiment Analysis: 

	NLTK VADER – Using VADER, I was able to detect the sentiment from each hotel review and compartmentalize them to three categories: POSTIVE, NEGATIVE, and NEUTRAL

Recommender Engine:

	Engine 1 (TF IDF + Topic Modeling) – Conducted topic modeling first then used Cosine distance to generate recommendation. Results from recommendation engine is okay, but not great.

	Engine 2 (TF IDF + Cosine Similarity Matrix) – After creating a TF-IDF matrix, I built a Cosine Similarity Matrix, and generated recommendation based on Cosine distance. Recommended result was great. Cafés would recommend other similar cafés. Bakeries would recommend other bakeries and desert places. Fast food recommended other fast food joints. 

Tools

Sklearn, Pandas, Numpy, Gensim, NLTK, and Scipy 

Communication

Slides and visuals are in PPT, submitted via PDF. 
