Gender Classification Using Support Vector Classifier (SVC)
This repository contains a machine learning project that predicts the gender of users based on their product viewing history and session duration using a Support Vector Classifier (SVC). The dataset used consists of user session information, including start and end times and the list of products viewed during each session.

Introduction
In this project, we aim to classify the gender of users based on their online product viewing behavior and session duration. By leveraging a bag-of-words representation of product lists and session duration as features, the model predicts whether a user is male or female.

Technologies Used:

Python
Scikit-learn (SVC for classification)
Pandas & NumPy (for data manipulation)
Matplotlib & Seaborn (for visualization)
Joblib (for model persistence)


Dataset
1.train.csv
Columns:
session_id: Unique session identifier
startTime: Start time of the session
endTime: End time of the session
ProductList: Products viewed during the session, separated by / and terminated with ;
gender: Target label (male or female)

2.test.csv
Columns:
session_id: Unique session identifier
startTime: Start time of the session
endTime: End time of the session
ProductList: Products viewed during the session, separated by '/' and terminated with ';'


Project Workflow
1. Data Preprocessing
Tokenization: The ProductList is tokenized into individual products.
Vectorization: The product list is transformed into a bag-of-words representation using CountVectorizer.
Feature Engineering: Session duration is calculated as the difference between endTime and startTime and used as an additional feature.
Label Encoding: The target column (gender) is encoded using LabelEncoder.
2. Model Training
Train a Support Vector Classifier (SVC) using a linear kernel.
Save the trained model, vectorizer, and label encoder for future use.
3. Model Evaluation
Evaluate the model's performance on a test dataset using metrics such as accuracy and a classification report.
4. Visualization
Plot graphs to visualize the classification results and session duration distribution:
Confusion Matrix: Shows the predicted vs actual gender.
Heatmap: Displays the average session duration for each actual vs predicted gender.
Histogram: Shows the distribution of session durations by gender.
