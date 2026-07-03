# 🌊 SONAR Rock vs Mine Prediction

A Machine Learning classification project that predicts whether an underwater object detected using SONAR signals is a **Rock** or a **Mine**.

The project uses **Logistic Regression** to classify SONAR signal data based on the reflected sound wave patterns received from underwater objects.

## 📌 Project Overview

SONAR (Sound Navigation and Ranging) is a technology that uses sound waves to detect and identify objects underwater.

In this project, a Machine Learning model is trained using SONAR signal data to predict whether the detected object is:

* 🪨 **Rock (R)**
* 💣 **Mine (M)**

The model learns patterns from SONAR signal measurements and performs binary classification.

## 📊 Dataset

The dataset contains SONAR signal data collected from underwater objects.

* Total samples: **208**
* Input features: **60 numerical SONAR signal values**
* Target classes:

  * **R** → Rock
  * **M** → Mine

Each row represents SONAR signals reflected from an underwater object.

## ⚙️ Machine Learning Workflow

The project follows a basic end-to-end Machine Learning workflow:

1. Import required Python libraries
2. Load the SONAR dataset
3. Explore and analyze the dataset
4. Separate features and target labels
5. Split the dataset into training and testing data
6. Train the Logistic Regression model
7. Evaluate the model using accuracy score
8. Build a prediction system for new SONAR input data

## 🤖 Machine Learning Model

### Logistic Regression

Logistic Regression is used as the classification algorithm in this project.

It is a supervised Machine Learning algorithm commonly used for binary classification problems.

In this project, the model predicts one of two classes:

`Rock` or `Mine`

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn
* Google Colab
* Jupyter Notebook

## 📚 Python Libraries

```python
import numpy as np
import pandas as pd

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score
```

## 📂 Project Structure

```text
SONAR-Rock-vs-Mine-Prediction/
│
├── rock_vs_mine_prediction.ipynb
└── README.md
```

## 🔍 Model Training

The dataset is divided into training and testing data using `train_test_split`.

The Logistic Regression model is trained on the training dataset.

```python
model = LogisticRegression()

model.fit(X_train, Y_train)
```

## 📈 Model Evaluation

The performance of the trained model is evaluated using the Accuracy Score.

```python
training_data_accuracy = accuracy_score(training_data_prediction, Y_train)

test_data_accuracy = accuracy_score(test_data_prediction, Y_test)
```

This helps measure how accurately the model predicts Rock and Mine SONAR signals.

## 🔮 Prediction System

The project also includes a prediction system that accepts new SONAR signal data.

The trained model predicts whether the underwater object is a Rock or a Mine.

Example prediction logic:

```python
prediction = model.predict(input_data_reshaped)

if prediction[0] == 'R':
    print('The object is a Rock')
else:
    print('The object is a Mine')
```

## ▶️ How to Run the Project

1. Clone this repository.

```bash
git clone https://github.com/Jayeshbirla/SONAR-Rock-vs-Mine-Prediction.git
```

2. Open the notebook in Google Colab or Jupyter Notebook.

3. Add the SONAR dataset.

4. Update the dataset file path if required.

5. Run all notebook cells.

## 🎯 What I Learned

Through this project, I gained hands-on experience with:

* Understanding a Machine Learning classification problem
* Working with Pandas and NumPy
* Data preprocessing and exploration
* Separating features and target labels
* Splitting data into training and testing sets
* Training a Logistic Regression model
* Evaluating model performance using accuracy score
* Building a prediction system for unseen input data

## 🚀 Future Improvements

Future improvements for this project may include:

* Comparing multiple Machine Learning algorithms
* Adding data visualization
* Performing feature scaling
* Using cross-validation
* Hyperparameter tuning
* Deploying the model using Streamlit

## 👨‍💻 Author

**Jayesh Birla**

AI & Machine Learning Enthusiast | M.Tech Student

GitHub: https://github.com/Jayeshbirla

---

⭐ If you found this project useful, feel free to star the repository.
