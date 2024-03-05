For this project, we will analyze recipes from Food.com with the goal to discover how well these recipes can be grouped by keyword and what information from a recipe is helpful to predict a recipe’s rating. A recipe’s rating is a signal of how popular a recipe is, so understanding what kinds of recipes are rated higher, which can be analyzed using keywords, will give us insight into which recipes are more popular. Since our dataset has columns containing nested data, such as lists, the main challenge with working with our dataset will be extracting the nested data to use. An additional challenge will be cleaning up the text data for a recipe’s instructions.

**Feature Engineering**

Before starting the analysis, we tried different methods in feature engineering, such as encoding the data, log transformation and normalization. 

**Supervised Learning**

We have applied a variety of supervised learning models, including Logistic Regression, XGBoost Classifier, and Neural Network, to analyze recipe data.

***Result***
| Model             | Mean Accuracy   | Standard Deviation of Accuracy |
|-------------------|-----------------|--------------------------------|
| Logistic Regression | 0.711985      | 0.025384                       |
| XGBoost           | 0.601814        | 0.001843                       |
| Neural Network    | 0.729215        | 0.001828                       |

| Model             | True Label | Prediction    |          |
|-------------------|------------|---------------|----------|
|                   |            |               |          |
| Logistic Regression | Negative | Negative      | 45%      |
|                   | Positive | Positive      | 26%      |
|                   |            |               |          |
| XGBoost           | Negative | Negative      | 37%      |
|                   | Positive | Positive      | 23%      |
|                   |            |               |          |
| Neural Network    | Negative | Negative      | 45%      |
|                   | Positive | Positive      | 28%      |


**Unsupervised Learning**

For unsupervised learning, we used clustering and topic modeling methods to discover properties of the dataset. In clustering, we utilized different methods to vectorize the natural language text of recipes and reviews then used Kmeans clustering to cluster the vectors. We vectorized the data using Sentence Transformers, Word2Vec, and TF-IDF. In topic modeling, we used Latent Dirichlet Analysis (LDA) and Singular Value Decomposition (SVD) for Latent Semantic Indexing (LSI).

***Clustering***
| Clustering Model                            | Cluster Size Ratio | Cluster Purity | NMI    |
|---------------------------------------------|---------------------|----------------|--------|
| KMeans                                      | 0.5984              | 0.6716         | 0.0232 |
| Agglomerative, with Euclidean distance      | 0.1643              | 0.6716         | 0.0013 |
| Agglomerative, with L2 distance             | 0.0006              | 0.6722         | 0.0021 |
| Agglomerative, with cosine distance         | 0.0006              | 0.6716         | 0.0007 |

***Topic Modeling***
| Rating | Recipes                                                                             | Reviews                                                                                                       |
|--------|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 5      | Small appliance, Stove top, Brunch, Breakfast, Savory, European, Kid friendly, Large groups, Lunch | Yum, Good, Fantastic, Easy to Make, Chocolate, Fudge, Cider                                             |
| 3      | Snacks, Lunch, Brunch, Breads, Potato, Kid friendly, Large groups, Dish            | Nothing spectacular, Good or bland flavor, Spices, Nutmeg, Cinnamon, Little time                          |
| 1      | Weeknight, Vegan, Summer, European, Quick, Small appliance, Cookie, Brownie, Dessert | Ok, Regular, Plain, Didn’t like, Hated, Offensive name for minorities                                      |
|        | Chicken, Poultry, Snacks, European, Dessert, Mexican, Breads, Kid friendly, Free   | N/A                                                                                                           |


*** A full result can be found in pdf file.
