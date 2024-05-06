# Recommendation Hybrid Model
## Project introduction:
<br>This is a project focusing on generate algorithms for a hybrid recommendation model.
<br>
## Data information:
<br> I use an available data set provided by a group of data professionals at UCSD. This data set contains product reviews and metadata that they scrapped from Amazon.
<br> The full data set span a period of 22 years, including ~233.1 million reviews up to Oct 2018 about all categories on Amazon. Reviews include product and user information, ratings, and a plaintext review. In this project, I'll work with a subset of the full data which focus only on Movies & TV category and has been reduced to extract the 5-core which include users and items have at least 5 reviews (13.7 mio reviews of Movies & TV category and 748k metadata about movies.)
<br>Data source: https://nijianmo.github.io/amazon/index.html
<br><b>Citation:</b>
<br>
Justifying recommendations using distantly-labeled reviews and fined-grained aspects
<br>Jianmo Ni, Jiacheng Li, Julian McAuley
<br>Empirical Methods in Natural Language Processing (EMNLP), 2019
## Data cleaning:
- Drop missing values
- Preprocess text data in ‘review’, product ‘description’ columns: lowercase, remove punctuation, remove digit, remove stopwords.
- Drop unnecessary columns: features, details, image, video, store, etc.
- Drop unrelated categories:
- Drop duplicates and Merge ‘review’ table with ‘metadata’ table on ‘parent_asin’.
## Data inspection (EDA):

<img src="https://github.com/ChiNguyen39/recommendation_hybrid_model/blob/main/chart/top%2020.png?raw=true" width=400>
Here is the chart of top 20 users who gave the biggest number of reviews. Well, the most active user gave more than 4000 reviews, it means he/she spend his/her life in watching movies & tv.!
<br>
<img src="https://github.com/ChiNguyen39/recommendation_hybrid_model/blob/main/chart/rating%20distribution.png?raw=true" width=400>
Here is the distribution chart of the rating the user gave. It seems that most of the user feel happy with their choice when the most rating are above 4.0
<br>
<img src="https://github.com/ChiNguyen39/recommendation_hybrid_model/blob/main/chart/word%20cloud.png?raw=true" width=400>
Here is the word cloud created from reviews the user wrote about movies they purchased. And we can see this is a nice picture when there are a lot of nice words in big size such as good movie, love, like, great, well,etc.

## Model algorithms:
There are two popular methods for recommendation systems:
- Collaborative filtering: User-based, Item-based
- Content-based filtering
<br><b>Firstly, I build algorithms for user-based filtering method to find out 5 similar users with the target user, the result of this method is the movies that similar user watched but target user not yet watched.
<br>
And these movies will be filtered out by content-based filtering algorithms to eliminate the less similar movies.</b>
<br> Here is the visualization of my algorithms:
<img src="https://github.com/ChiNguyen39/recommendation_hybrid_model/blob/main/chart/Slide15.jpeg?raw=true" width=700>
<br> <b>Link to my recorded presentation: https://drive.google.com/drive/folders/1iYSeU4Jew8EmMyHCmjm4umNq-TfF3jc3?usp=sharing









