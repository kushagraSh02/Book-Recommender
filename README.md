# Book-Recommendation-System
 A Book Recommender, for people who want to find similar books to one they like.

First we preprocess the data like removing null values, image urls, duplicate entries etc from all three data files. Then we divide the dataset based on explicit and implicit ratings. 

Explicit ratings are those ratings that the user rates him/herself for hte product. Implicit ratings are those ratings that the user does not rate directly but are  calculated based on preference of the user.

Then we apply 5 approaches to recommend books to the user:

1. **Collaborative Filtering**: Considering user ratings to find cosine similarities in ratings by several users to recommend books.

2. **Correlation Based Recommendation**: Created a correlation matrix considering only those books which have total ratings of more than 50. Then a user-book rating matrix is created. For the input book using the correlation matrix, top books are recommended.

3. **Nearest Neighbour Recommendation**: Created a compressed sparse row matrix taking ratings of each Book by each User individually. This matrix is used to train the Nearest Neighbours model and then finds n nearest neighbors using the cosine similarity metric.

4. **Content Based Recommendation**: Recommend books by calculating similarities in Book Titles. TF-IDF vectors were created for unigrams and bigrams of Book-Titles. (only those books' data has been considered which are having at least 80 ratings)

5. **Hybrid Approach(Content+Collaborative)**: Using the combination of content-based filtering and collaborative filtering system. A percentile score is given to the results obtained from both content and collaborative filtering models and is combined to recommend top n books.

### **Dependencies**
```
1. Scikit-learn
2. Seaborn
3. Matplotlib
4. numpy
5. Scipy
6. pandas
```
