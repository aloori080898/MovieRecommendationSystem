# MovieRecommendationSystem
Movie Recommendation System using Collaborative Filtering with Surprise Library

Objective:
The goal of this machine learning project is to build a movie recommendation system utilizing collaborative filtering techniques. The collaborative filtering approach predicts a user's preferences by collecting preferences from many users (collaborating). In this project, the Surprise library is employed for its ease of use in building and evaluating collaborative filtering models.

Dataset:
The MovieLens dataset (small version) is used for this project. It contains user ratings for various movies, providing a rich source of information for collaborative filtering.

Data Loading and Preprocessing:
The dataset is loaded, and necessary preprocessing steps are performed using the Pandas library.
The Surprise library's specific data format is created using the Reader and Dataset classes.

Train-Test Split:
The dataset is split into training and testing sets to evaluate the model's performance.

Hyperparameter Tuning:
The KNNBasic collaborative filtering algorithm is chosen for its simplicity and effectiveness.
A parameter grid is defined for hyperparameter tuning, exploring different values for 'k' (neighborhood size) and similarity options (cosine similarity, user-based).
GridSearchCV is employed to find the optimal hyperparameters based on root mean square error (RMSE) as the evaluation metric.

Model Training:
The model is trained using the best hyperparameters obtained from the grid search.

Model Evaluation:
The model's performance is evaluated on the test set using RMSE.

Movie Recommendations:
For a specific user (example user_id = 1), the system generates movie recommendations.
The user's preferences are considered, and movies they have already rated are excluded.
Predictions are made for unrated movies, sorted by estimated ratings in descending order.
The top N recommendations are displayed.

Technologies Used:
Python, Pandas for data manipulation
Surprise library for collaborative filtering
GridSearchCV for hyperparameter tuning
Evaluation metrics: RMSE (Root Mean Square Error)

Outcome:
The implemented movie recommendation system effectively predicts user preferences, providing personalized movie suggestions. Hyperparameter tuning enhances model accuracy, contributing to an improved user experience in the movie-watching domain.
