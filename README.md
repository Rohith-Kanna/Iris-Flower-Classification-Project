# 🌸 Iris Flower Classification Web App

An end-to-end Machine Learning web application that predicts the species of an Iris flower based on user-provided measurements.

This project was built to understand the **complete ML workflow — from model training to deployment**.

🔗 **Live Application**  
https://ml-model-deployment-irisdetection.streamlit.app/

---

# 📌 Project Overview

The goal of this project was to move beyond training models in notebooks and build a **complete ML application**.

The project covers the full pipeline:

1. Data exploration and preprocessing  
2. Training machine learning models  
3. Saving trained models for reuse  
4. Building an interactive web application  
5. Adding login and signup functionality  
6. Storing user data using a database  
7. Deploying the application online  

---

# 🧠 Machine Learning Models Used

Two models were trained and used in the application.

## Random Forest Classifier
- Ensemble learning method
- Uses multiple decision trees
- Provides strong performance on structured data

## Logistic Regression
- Linear classification model
- Fast and interpretable
- Used as a baseline model

The trained models were saved using **pickle** and loaded into the Streamlit application for predictions.

---

# 🌼 Dataset

The project uses the classic **Iris Flower Dataset**.

### Input Features
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

### Target Classes
- Iris-setosa
- Iris-versicolor
- Iris-virginica

---

# 🖥️ Application Features

## 👤 User Authentication
- Users can **sign up and create an account**
- Existing users can **log in**
- User credentials are stored in the database

## 🌸 Flower Prediction
Users can:

1. Enter flower measurements
2. Choose a prediction model
3. Get the predicted Iris species

## 📊 Prediction History
Every prediction made by a user is stored and displayed.

The history shows:
- Input values
- Selected model
- Predicted species
- Timestamp

---

# 🗄️ Database

The application uses **SQLite** as a lightweight database.

Two tables are used:

### Users Table
Stores login credentials.

```
users
-----
id
username
password
created_at
```

### Predictions Table
Stores user prediction history.

```
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
```

SQLite was chosen because it is **lightweight, simple, and does not require a server**.

---

# ⚙️ Technologies Used

### Programming
- Python

### Machine Learning
- scikit-learn
- pandas
- numpy

### Web Application
- Streamlit

### Database
- SQLite

### Version Control
- Git
- GitHub

### Deployment
- Streamlit Community Cloud

---

# 📂 Project Structure

```
ML-Model-Deployment/
│
├── app.py
├── iris_app.db
├── label_encoder.pkl
├── random_forest_model.pkl
├── logistic_regression_model.pkl
├── IrisDataSet.csv
├── MLModelTrain.ipynb
├── requirements.txt
└── README.md
```

---

# 🚀 Running the Project Locally

### 1. Clone the repository

```
git clone https://github.com/Rohith-Kanna/ML-Model-Deployment.git
cd ML-Model-Deployment
```

### 2. Install dependencies

```
pip install -r requirements.txt
```

### 3. Run the application

```
streamlit run app.py
```

The web app will open in your browser.

---

# 🌍 Deployment

The project is deployed using **Streamlit Community Cloud**.

Deployment process:

1. Push project to GitHub
2. Add a `requirements.txt`
3. Connect repository to Streamlit Cloud
4. Deploy the Streamlit application

---

# ⚠️ Security Note

Passwords in this project are stored in **plain text** for learning purposes.

In real-world applications, passwords should be **hashed using libraries such as bcrypt**.

---

# 📈 Future Improvements

Possible improvements for this project:

- Password hashing for improved security
- Admin dashboard
- Data visualizations
- Additional machine learning models
- Cloud database integration
- Multi-page Streamlit application

---

# 👨‍💻 Author

**Rohith Kanna Gv (RK)**  
Computer Science Engineering Student

---

⭐ If you found this project interesting, feel free to **star the repository**.
