# 🎓 Student Performance Predictor

## 📌 Overview
This project focuses on predicting **student academic performance** based on demographic and lifestyle attributes.  
Using a dataset with factors such as **gender, ethnicity, parental education, lunch type, and test preparation**, the goal is to forecast student **math, reading, and writing scores** through machine learning regression models.  

The project evaluates multiple models and benchmarks their predictive power to identify the most reliable approach.

---

## 📊 Dataset Description
The dataset includes the following columns:

- **gender** – Student gender  
- **race_ethnicity** – Student’s ethnic background  
- **parental_level_of_education** – Parent’s highest education level  
  - Options: `associate's degree`, `bachelor's degree`, `high school`, `master's degree`, `some college`, `some high school`  
- **lunch** – Type of lunch (`free/reduced`, `standard`)  
- **test_preparation_course** – Completion status of prep course  
- **math_score** – Math exam score  
- **reading_score** – Reading exam score  
- **writing_score** – Writing exam score  

---

## 🚀 Models Trained & Results

### 🔹 Linear Regression
- **Train:** RMSE 5.34 | MAE 4.27 | R² 0.8735  
- **Test:** RMSE 5.42 | MAE 4.22 | R² 0.8792 ✅  

### 🔹 Lasso
- **Train:** RMSE 6.59 | R² 0.8071  
- **Test:** RMSE 6.52 | R² 0.8253  

### 🔹 Ridge
- **Train:** RMSE 5.32 | R² 0.8743  
- **Test:** RMSE 5.39 | R² 0.8806 ✅ (Best among linear models)  

### 🔹 K-Neighbors Regressor
- **Train:** RMSE 5.71 | R² 0.8554  
- **Test:** RMSE 7.26 | R² 0.7835  

### 🔹 Decision Tree
- **Train:** RMSE 0.27 | R² 0.9997 (Overfitting)  
- **Test:** RMSE 7.35 | R² 0.7778  

### 🔹 Random Forest Regressor
- **Train:** RMSE 2.28 | R² 0.9769  
- **Test:** RMSE 5.99 | R² 0.8527  

### 🔹 XGBRegressor
- **Train:** RMSE 1.01 | R² 0.9955  
- **Test:** RMSE 6.47 | R² 0.8278  

### 🔹 CatBoost Regressor
- **Train:** RMSE 3.04 | R² 0.9589  
- **Test:** RMSE 6.01 | R² 0.8516  

### 🔹 AdaBoost Regressor
- **Train:** RMSE 5.84 | R² 0.8485  
- **Test:** RMSE 6.21 | R² 0.8413  

📌 **Observation:**  
- **Ridge Regression** shows the most stable and best generalization with **R² ≈ 0.88**.  
- Tree-based models like **Random Forest, CatBoost, and AdaBoost** also perform competitively.  
- **Decision Tree & XGBoost** exhibit signs of overfitting.  

---

## 🛠️ Tech Stack
- **Python**
- **Flask** (for deployment)
- **NumPy**, **Pandas**, **Seaborn**, **Matplotlib**
- **Scikit-learn**
- **CatBoost**, **XGBoost**
- **Dill** (model serialization)

---

## 📂 Project Structure
```bash
ML-Student_Performance_Predictior/
├── artifacts/ # Saved models, metrics, reports, etc.
├── catboost_info/ # CatBoost training logs and artifacts
├── notebook/ # Exploratory data analysis & experiments
├── src/ # Source code for data processing, model training, inference
├── templates/ # HTML templates for Flask app frontend
├── app.py # Main Flask application script
├── requirements.txt # Project dependencies
├── setup.py # Setup configuration for installation
├── README.md # Project documentation
└── .gitignore # Files/folders to ignore in Git
```
## 🚀 How to Run

Follow these steps to set up and run the project locally:

1. **Clone the repository**
   ```bash
   git clone https://github.com/DipeanDas/ML-Student_Performance_Predictior.git
   cd ML-Student_Performance_Predictior
2. **Create and activate a virtual environment**
   ```
   python -m venv venv
   source venv/bin/activate    # On Linux/Mac
   venv\Scripts\activate       # On Windows
   ```
3. **Install dependencies**
   ```
   pip install -r requirements.txt
4. **Run the Flask app**
   ```
   python app.py
   ```
## Project By
  **Dipean Dasgupta**<br>
  **Data Analyst & AIML Enthusiast**
