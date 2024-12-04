**﻿Gender Classification Using Support Vector Classifier (SVC)**

This repository contains a machine learning project that predicts the gender of users based on their product viewing history and session duration using a Support Vector Classifier (SVC). The dataset used consists of user session information, including start and end times and the list of products viewed during each session.

**Introduction**

In this project, we aim to classify the gender of users based on their online product viewing behavior and session duration. By leveraging a bag-of-words representation of product lists and session duration as features, the model predicts whether a user is male or female.

**Technologies Used:**

Python
Scikit-learn (SVC for classification)
Pandas & NumPy (for data manipulation)
Matplotlib & Seaborn (for visualization)
Joblib (for model persistence)


**Dataset**

1.train.csv
**Features:**
session_id: Unique session identifier
startTime: Start time of the session
endTime: End time of the session
ProductList: Products viewed during the session, separated by / and terminated with ;
gender: Target label (male or female)

2.test.csv
**Features:**
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
![8d3d9cc2-3d3c-4a8a-b183-b4d92fd7b5df](https://github.com/user-attachments/assets/4c0cad6a-6f0b-4991-9e18-f876ae1d7f7a)

Heatmap: Displays the average session duration for each actual vs predicted gender.
![f574dfe9-4bb2-4a34-9150-1db3f691b258](https://github.com/user-attachments/assets/015a24a6-8acc-406f-b72a-797b5c546a54)

**Note**

Due to the large size of the trained model files, they could not be uploaded to GitHub. Please run the code locally to train and build the model on your system.

**Conclusion**

This Gender Classification project uses Support Vector Classification (SVC) to predict the gender of users based on their product list interaction and session duration. The model utilizes a custom tokenizer to process product lists, converting them into a bag-of-words representation for the classifier. The session duration is also used as an additional feature to improve prediction accuracy.

Key features of the project:

SVC Model: Linear kernel SVC was used for classification.
Custom Tokenization: A custom tokenizer splits product IDs and removes any unwanted symbols like ;.
Session Duration: The time between user actions is calculated and used as a feature for prediction.
Model Persistence: Trained model and preprocessing components (vectorizer, label encoder) are saved and can be reloaded for future use.
Evaluation: The model was evaluated using classification metrics like accuracy and F1-score.
By utilizing these techniques, this project demonstrates how to apply machine learning for gender classification using user interaction data. It can be extended to other prediction tasks or improved with more features or data.

