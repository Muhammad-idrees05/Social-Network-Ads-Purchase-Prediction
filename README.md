# 📱 Social Network Ads Purchase Prediction Using Logistic Regression

## 📌 Project Overview

This project uses Machine Learning to predict whether a user will purchase a product after being exposed to social network advertisements.

It implements **Logistic Regression**, a supervised classification algorithm, to analyze user demographic and financial information and predict purchasing behavior.

The project includes Exploratory Data Analysis (EDA), categorical encoding, correlation analysis, model training, classification evaluation, and predictions on new user records.

## 🎯 Project Objectives

- Analyze user purchasing behavior based on demographic information.
- Explore relationships between age, gender, estimated salary, and purchases.
- Visualize purchasing patterns across different user groups.
- Encode categorical variables into numerical representations.
- Train a Logistic Regression classification model.
- Evaluate classification performance using standard metrics.
- Predict purchasing behavior for unseen users.

## 📂 Dataset

**Dataset:** Social Network Ads Dataset.

The dataset contains user information and purchasing decisions.

### Input Features

| Feature | Description |
|---|---|
| User ID | Unique identifier assigned to each user |
| Gender | User's gender |
| Age | User's age |
| EstimatedSalary | Estimated annual salary |

### Target Variable

`Purchased`

- `0` – User did not purchase the advertised product.
- `1` – User purchased the advertised product.

## 🛠️ Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 🔍 Exploratory Data Analysis (EDA)

The project performs several visualizations to understand user purchasing patterns.

### Visualizations Included

1. **Gender vs Purchases:** Bar chart showing purchases grouped by gender.
2. **Age vs Purchases:** Visualizes purchasing behavior across different age groups.
3. **Estimated Salary Distribution:** Histogram exploring salary distribution.
4. **Correlation Heatmap:** Shows correlations between numerical dataset features.

These visualizations help explore relationships between user characteristics and purchasing decisions.

## ⚙️ Data Preprocessing

### 1. Data Inspection

- Load the dataset using Pandas.
- Inspect dataset records.
- Check for missing values.
- Explore feature distributions.

### 2. Categorical Encoding

`OrdinalEncoder` is used to convert the `Gender` column into numerical values suitable for model training.

### 3. Feature and Target Separation

- Input features (`X`): All columns except `Purchased`.
- Target (`y`): `Purchased`.

### 4. Train-Test Split

The dataset is divided into:

- Training data: 80%
- Testing data: 20%
- Random state: 42

## 🤖 Machine Learning Model

### Logistic Regression

The project uses Logistic Regression to classify users into two purchasing categories.

Logistic Regression estimates the probability of a user purchasing a product based on the input features.

The sigmoid function is used to convert the model's output into a probability:

\[
P(y=1|X)=\frac{1}{1+e^{-z}}
\]

Where:

- \(P(y=1|X)\) represents the probability of purchasing.
- \(z\) represents the weighted combination of input features.

The predicted class is determined using the model's default classification threshold.

## 📊 Model Evaluation

The model is evaluated using the following metrics:

- **Accuracy Score:** Measures the proportion of correct predictions.
- **Precision Score:** Measures how many predicted purchases are actually purchases.
- **Classification Report:** Provides precision, recall, F1-score, and support for each class.

The model's predictions are compared against the actual test labels to evaluate classification performance.

## 🔮 Prediction on New Users

The trained Logistic Regression model is used to predict purchasing behavior for new user records.

Example:

```python
new_data = pd.DataFrame({
    'User ID': [15624510, 15810944],
    'Gender': [1.0, 1.0],
    'Age': [27, 46],
    'EstimatedSalary': [57000, 28000]
})

new_data_pred = Log_reg.predict(new_data)

print(new_data_pred)
```

The model returns:

- `0` – User is predicted not to purchase.
- `1` – User is predicted to purchase.

## 🚀 Installation and Usage

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/social-network-ads-prediction.git
```

### 2. Navigate to the Project Directory

```bash
cd social-network-ads-prediction
```

### 3. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 4. Run the Notebook

```bash
jupyter notebook
```

Open the project notebook and execute the cells to perform data analysis, train the Logistic Regression model, evaluate predictions, and classify new users.

## 📁 Project Structure

```text
Social-Network-Ads-Prediction/
│
├── logistic regression dataset-Social_Network.csv
├── Social_Network_Ads_Prediction.ipynb
├── README.md
│
└── requirements.txt
```

## 🔧 Future Improvements

- Remove irrelevant identifiers such as `User ID` from model training.
- Apply StandardScaler to numerical features.
- Use stratified train-test splitting.
- Evaluate the model using a confusion matrix and ROC-AUC.
- Compare Logistic Regression with KNN, Decision Trees, and Random Forest.
- Apply cross-validation and hyperparameter tuning.
- Build an interactive prediction application using Streamlit or Flask.

## 👨‍💻 Author

**Muhammad Idrees**  
AI & Machine Learning Developer

Interested in Machine Learning, Deep Learning, Computer Vision, NLP, and AI-powered applications.

⭐ If you find this project useful, consider giving the repository a star!
