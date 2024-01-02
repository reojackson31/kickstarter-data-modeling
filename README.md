# Classification and Clustering on Kickstarter projects
##### *- Project for MMA INSY662 - Data Mining & Visualization, McGill University*

## Introduction and Business Use Case
Kickstarter is a crowdfunding platform that connects creators with supporters worldwide. The first part of this project is focused on building a classification model to predict if a project would be successful before its launch. This model would be helpful for project owners, providing them with insights on the best combination of project attributes to increase their chances of getting funded. The second part of this project involves building a clustering model to group projects based on their attributes, which could have many applications like allowing Kickstarter employees analyze the type of projects on their platform, helping them in the verification process of new projects, or allowing them to identify specific type of projects that need special assistance.

## Classification Model - Model Selection
The dataset is split into train and test sets in 2:1 ratio, and modeled using different classification models including Logistic Regression, KNN, Decision Trees, Random Forest, Gradient Boosting, and Artificial Neural Network. Following this, hyperparameter tuning is done for each model using GridSearchCV. Gradient Boosting model was selected with the best set of hyperparameters since it gave the highest accuracy of 74.5%.
| Classification Model     | Accuracy with Train-Test split (2:1) |
| ------------------------ |:------------------------------------:|
| Logistic Regression      |                 68.2%                |
| KNN                      |                 67.7%                |
| Decision Trees           |                 70.4%                |
| Random Forest            |                 72.8%                |
| Gradient Boosting        |                 74.5%                |
| Artificial Neural Network|                 71%                  |


## Classification Model - Insights
The features that are most important to predict the project success are project goal, category, duration between the project creation and launch, duration between the project launch and deadline, and length of the project name. So, a project owner should carefully evaluate these features of their project to maximize the chance of success. 

## Clustering Model - Finding Optimal Number of clusters
To find the optimal number of clusters for the model, three approaches are used – Elbow Method, Silhouette Score, and Pseudo F-statistics. Using these methods, a cluster size of four is selected since it gave the best results, with a Silhouette score of 0.41, suggesting valid evidence of the clustering fit to reality.

## Clustering Model - Insights
Using k-means clustering, four clusters are created with varying sizes depending on the project attributes:
- Cluster 1 – Quick to Launch, Higher Ambitions
- Cluster 2 – Balanced and Moderate
- Cluster 3 – Shorter Yet Ambitious
- Cluster 4 – Unconventional and Non-US Centric
