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
[Top20 user][https://github.com/ChiNguyen39/recommendation_hybrid_model/blob/main/chart/top%2020.png?raw=true]



