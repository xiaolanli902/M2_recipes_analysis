**Recipes Analysis**

For this project, we will analyze recipes from Food.com with the goal to discover how well these recipes can be grouped by keyword and what information from a recipe is helpful to predict a recipe’s rating. A recipe’s rating is a signal of how popular a recipe is, so understanding what kinds of recipes are rated higher, which can be analyzed using keywords, will give us insight into which recipes are more popular. Since our dataset has columns containing nested data, such as lists, the main challenge with working with our dataset will be extracting the nested data to use. An additional challenge will be cleaning up the text data for a recipe’s instructions.

***Feature Engineering:***
Before starting the analysis, we tried different methods in feature engineering, such as encoding the data, log transformation and normalization. 

***Supervised learning:***
We have applied a variety of supervised learning models, including Logistic Regression, XGBoost Classifier, and Neural Network, to analyze recipe data.

****Result****
| Model             | Mean Accuracy   | Standard Deviation of Accuracy |
|-------------------|-----------------|--------------------------------|
| Logistic Regression | 0.711985      | 0.025384                       |
| XGBoost           | 0.601814        | 0.001843                       |
| Neural Network    | 0.729215        | 0.001828                       |

| Model               | True Label | Prediction | Negative | Positive |
|---------------------|------------|------------|----------|----------|
| Logistic Regression | Negative   | Negative   | 45%      | 7%       |
|                     |            | Positive   | 22%      | 26%      |
| XGBoost             | Negative   | Negative   | 37%      | 15%      |
|                     |            | Positive   | 25%      | 23%      |
| Neural Network      | Negative   | Negative   | 45%      | 7%       |
|                     |            | Positive   | 20%      | 28%      |
