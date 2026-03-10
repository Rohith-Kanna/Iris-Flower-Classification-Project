🌸 Iris Flower Classification Web App

An end-to-end Machine Learning web application that predicts the species of an Iris flower based on user-provided measurements.
This project was built as a hands-on learning exercise to understand the complete ML workflow — from model training to deployment.

The application allows users to sign up, log in, enter flower measurements, choose a model, and view their prediction history.

🔗 Live Application:
https://ml-model-deployment-irisdetection.streamlit.app/

📌 Project Overview

The goal of this project was to move beyond training models in notebooks and learn how to deploy a machine learning model as an interactive web application.

The project covers the full pipeline:

Data exploration and preprocessing

Training multiple machine learning models

Saving trained models using serialization

Building an interactive user interface

Adding authentication functionality

Storing user data and predictions using a database

Deploying the application to the web

🧠 Machine Learning Models Used

Two models were implemented and compared:

Random Forest Classifier

Ensemble learning method

Uses multiple decision trees

Produces strong performance on structured data

Logistic Regression

Linear classification model

Fast and interpretable

Good baseline model

Both models were trained using the Iris dataset, and the trained models were saved using pickle so they could be reused in the web application.

🌼 Dataset

The project uses the classic Iris Flower Dataset, which contains measurements of iris flowers.

Features used for prediction

Sepal Length

Sepal Width

Petal Length

Petal Width

Target

Iris-setosa

Iris-versicolor

Iris-virginica

🖥️ Application Features

The deployed web application provides the following functionality:

👤 User Authentication

Users can sign up and create an account

Existing users can log in

User credentials are stored in a database

🌸 Flower Prediction

Users can enter:

Sepal Length

Sepal Width

Petal Length

Petal Width

They can also choose which model to use:

Random Forest

Logistic Regression

The application then predicts the species of the iris flower.

📊 Prediction History

Every prediction made by a user is stored in the database.

Users can view:

Input values used

Model selected

Predicted species

Timestamp of prediction

🗄️ Database

This project uses SQLite as a lightweight database.

Two tables are used:

Users Table

Stores login credentials.

users
-----
id
username
password
created_at
Predictions Table

Stores user prediction history.

predictions
-----------
id
username
sepal_length
sepal_width
petal_length
petal_width
predicted_species
model_used
timestamp

SQLite was chosen because it is simple, lightweight, and does not require a separate database server.

⚙️ Technologies Used
Programming

Python

Machine Learning

scikit-learn

pandas

numpy

Web Application

Streamlit

Database

SQLite

Version Control

Git

GitHub

Deployment

Streamlit Community Cloud

📂 Project Structure
ML-Model-Deployment/
│
├── app.py                         # Streamlit web application
├── iris_app.db                    # SQLite database
├── label_encoder.pkl              # Saved label encoder
├── random_forest_model.pkl        # Trained Random Forest model
├── logistic_regression_model.pkl  # Trained Logistic Regression model
├── IrisDataSet.csv                # Dataset
├── MLModelTrain.ipynb             # Model training notebook
├── requirements.txt               # Dependencies
└── README.md                      # Project documentation
🚀 How to Run the Project Locally
1. Clone the repository
git clone https://github.com/Rohith-Kanna/ML-Model-Deployment.git
cd ML-Model-Deployment
2. Install dependencies
pip install -r requirements.txt
3. Run the Streamlit application
streamlit run app.py

The application will open in your browser.

🌍 Deployment

The application is deployed using Streamlit Community Cloud, which allows quick deployment of Python apps directly from GitHub.

Deployment steps included:

Push project to GitHub

Create a requirements.txt

Connect repository to Streamlit Cloud

Deploy the app

⚠️ Security Note

Passwords in this project are stored in plain text for learning purposes.

In real-world applications, passwords should be securely hashed using tools such as bcrypt.

📈 Future Improvements

Some possible improvements for this project include:

Password hashing for improved security

Admin dashboard for viewing overall predictions

Graph-based visualization of user inputs

Adding more ML models

Migrating to a cloud database

Multi-page Streamlit application


⭐ If you found this project interesting

Feel free to star the repository and try out the live application!
