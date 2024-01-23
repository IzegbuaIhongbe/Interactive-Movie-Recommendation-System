# Interactive Movie Recommendation System (Collaborative Filtering)

The aim of this project is to build an interactive movie recommendation engine, where we can type in a movie title and receive a list of movies which we would like. The recommendations are based on the movie ratings made by users who like the same movies as we do.

We begin by reviewing our data and making any adjustments we require; in this project we remove any characters which would flaw our search engine from the movie titles. We create a string cleaning function using the python regular expression library and apply the function to the movie dataset titles. 

Once our movie titles are 'cleaned', we create a term/word frequency matrix for the movie title which assigns value/vector to the unique values or words in the titles and compares the values to other titles for our search engine to return a similarity score against other movie titles in the dataset calculated by our matrix, these calculations are done with the tfidvectorizer. It will not only look at single word but also word sequences to make search more accurate.

After our search function enabled by our matrix is created, we create a widget as our visual interface where we can type in our movie title to be searched. We also create a function which will enable us to search the movie data base and display the search results. This will complete the first part of the search engine.

In the next part of the project, we build the recommendation system which would be based on movie ratings made by users who like the same movie we search for, sort of a user generated recommendation. This is useful in recommending content across content driven sites.

We first find the users who like the movie we search for and find other movies they rated highly and find the movies all users rated highly; we then find the difference in the 'all users' vs 'similar users' groups to ensure the recommendations are specific to similar users' movie preference rather than all highly rated movies. Using this difference, we create a function calculate the percentage score of how good the recommendation will be and use the function to assign scores to the movies based on the searched movie title.

We create function to find similar movies for recommendation by combining the above functions and widget to give us a working in-notebook interface where we can type in a movie title and receive a list of similar movies we would like.

# Data

The link to the movie data set can be found here [Movie Dataset](https://files.grouplens.org/datasets/movielens/ml-25m.zip)

This dataset (ml-25m) describes 5-star rating and free-text tagging activity from [MovieLens](http://movielens.org), a movie recommendation service. It contains 25000095 ratings and 1093360 tag applications across 62423 movies. These data were created by 162541 users between January 09, 1995 and November 21, 2019. This dataset was generated on November 21, 2019.

Users were selected at random for inclusion. All selected users had rated at least 20 movies. No demographic information is included. Each user is represented by an id, and no other information is provided.

The data are contained in the files `genome-scores.csv`, `genome-tags.csv`, `links.csv`, `movies.csv`, `ratings.csv` and `tags.csv`.

The project currently makes use of the `movies.csv` and `ratings.csv` files.

### Data Pre-Processing

* The data is provided structured and cleaned, pre-processing steps are not majorly required, however we may drop or restructure some parts of the data as needed during the project.
