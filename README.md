# KNN Movie Recommendation ML

Please see the following for an introduction to the k-Nearest Neighbors Machine Learning Algorithm.

[https://www.analyticsvidhya.com/blog/2018/03/introduction-k-neighbours-algorithm-clustering/](https://www.analyticsvidhya.com/blog/2018/03/introduction-k-neighbours-algorithm-clustering/)

This is an exmaple of a content based, k-nearest neighbours Recommender system. "K-NN is a lazy learner because it doesn’t learn a discriminative function from the training data but “memorizes” the training dataset instead" [ref](https://sebastianraschka.com/faq/docs/lazy-knn.html). Unsupervised in this context. 

>Approaches
>Recommender systems can be loosely broken down into three categories: content based systems, collaborative filtering systems, and hybrid systems (which use a combination of the other two).
>
>Collaborative filtering approach builds a model from a user’s past behaviors (items previously purchased or selected and/or numerical ratings given to those items) as well as similar decisions >made by other users. This model is then used to predict items (or ratings for items) that the user may have an interest in.

>Hybrid approach combines the previous two approaches. Most businesses probably use hybrid approach in their production recommender systems.
>In this post, we are going to start with the most common approach, collaborative filtering, with a simple vanilla version. In the future posts, we will develop more advanced and sophisticated >methods to further improve our recommender’s performance and scalability.

![reco](https://user-images.githubusercontent.com/81447748/119277351-06d7ae80-bc17-11eb-82cc-7dd4878afe00.png)

The following resource shows an Item-Based Collaborative Filtering Recommender System. 

[https://towardsdatascience.com/prototyping-a-recommender-system-step-by-step-part-1-knn-item-based-collaborative-filtering-637969614ea](https://towardsdatascience.com/prototyping-a-recommender-system-step-by-step-part-1-knn-item-based-collaborative-filtering-637969614ea)


## Data 

This data was sourced from imdb.com, the link for which can be found below.  

"IMDb is an online database of information related to films, television programs, home videos, video games, and streaming content online..."

IMDb Datasets
Subsets of IMDb data are available for access to customers for personal and non-commercial use.

Context:

[https://www.imdb.com/interfaces/](https://www.imdb.com/interfaces/)

Specifically for the following files. 

- title.basics.tsv.gz
- title.ratings.tsv

Which can be downloaded from the link below (must be decompressed to tsv file format). 

[https://datasets.imdbws.com/](https://datasets.imdbws.com/)

    
## How to run

Use the Jupyter Notebook provided ( .ipynb file extension). 
 
## Pipeline 

The script goes through the steps below. 

 1. Load data 
 2. Visualizing the data 
 3. Cleansing the data (334,985 observations)
 4. Creates a feature vector for the genre 
 5. Appends to the feature vector, additional features 'isAdult', 'startYear', 'runtimeMinutes', 'averageRating', 'numVotes'
 6. Uses the sklearn MinMaxScaler() for scaling features as it scales the values from 0–1
 7. Fits the NearestNeighbors model with default distance metric ’minkowski’ and ‘brute’ will use a brute-force search
 8. Test some the top 5 most voted movies 

## Example output 

![Capture](https://user-images.githubusercontent.com/81447748/119276776-dfcbad80-bc13-11eb-85c0-f883347df08e.PNG)

## Requirements

Relevant package requirements are the first cell within the Jupyter Notebook. 
