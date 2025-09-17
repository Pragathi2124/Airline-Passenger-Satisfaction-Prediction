# Airline-Passenger-Satisfaction-Prediction
## Predicting Airline Passenger Satisfaction ✈️
**Machine Learning project to predict passenger satisfaction based on service features, travel attributes, and customer demographics.**

## ✈️ Project Aim
The airline industry faces the constant challenge of maintaining customer satisfaction in a highly competitive market. This project aims to solve this by building a robust predictive model that classifies passengers as "satisfied" or "dissatisfied/neutral."

The primary objectives are:
> Identify critical service attributes that most significantly influence passenger satisfaction.
> Build and evaluate multiple machine learning models to find the most accurate predictor.
> Provide actionable insights to airline management on which service areas to prioritize for investment to enhance customer loyalty and profitability.

## 📊 Dataset
- **Source**: Airline Passenger Satisfaction Survey dataset.  
- **Features**: 22 input variables.  
  - Demographics: Gender, Age, Customer Type.  
  - Travel Info: Class, Type of Travel, Flight Distance.  
  - Service Ratings: Wi-Fi, Seat Comfort, Food, Inflight Entertainment, Cleanliness, etc.  
  - Operational: Departure Delay, Arrival Delay.  
- **Target**: `Satisfaction` (Satisfied / Neutral or Dissatisfied).  

## ⚙️ Methodology & Workflow
The project followed a structured data science lifecycle, from initial exploration to final model deployment and interpretation.

**1. Data Cleaning and Preprocessing**
-**Handled Missing Values**: The Arrival Delay in Minutes column had a small number of missing values, which were imputed with the mean to maintain data integrity.
-**Data Type Conversion**: Ensured all numerical columns were of the correct data type for analysis and modeling.
**Label Encoding**: The categorical target variable satisfaction was converted into a numerical format (1 for Satisfied, 0 for Neutral/Dissatisfied) using LabelEncoder.

**2. Exploratory Data Analysis (EDA) & Key Insights**
-**Univariate & Bivariate Analysis**: Visualizations were created to understand the distribution of each feature and its relationship with passenger satisfaction.

Key Insights Discovered:
-**Travel Class**: Business class passengers reported significantly higher satisfaction rates than Economy and Economy Plus passengers.
-**Customer Loyalt**y: Loyal customers were more likely to be satisfied.
-**Service Quality**: Features like Inflight entertainment, Seat comfort, and On-board service showed a strong positive correlation with satisfaction.
-**Flight Delays:** Departure and arrival delays were strongly correlated with dissatisfaction.

**3. Feature Engineering and Selection**
-**Correlation Analysis:** A heatmap was generated to identify and analyze multicollinearity between features. High correlations were noted between Departure Delay and Arrival Delay, as expected.
-**Feature Importance:** After model training, feature importance was extracted, revealing that Inflight wifi service, Online boarding, and Type of Travel were among the top predictors.

**4. Model Building and Evaluation**
A comparative study of six different classification algorithms was conducted to identify the best-performing model.
> The data was split into training (80%) and testing (20%) sets.
> Models were trained and evaluated based on Accuracy, Precision, Recall, and F1-Score.


## 📈 Results

- **Best Model**: Random Forest Classifier.  
- **Performance**:  
  - Accuracy: **95.8%**  
  - High precision/recall balance.  
  - Confusion matrix showed strong classification of both satisfied and dissatisfied classes.
 
**    Model           |  Accuracy  | Precision | Recall  | F1-Score**
_________________________________________________________________
> Random Forest       |  95.8%     | 0.96      | 0.97    |  0.96
_________________________________________________________________
> XGBoost             |  94.6%     | 0.95      |  0.96   |  0.95
_________________________________________________________________
> Decision Tree       |  93.9%     | 0.94      | 0.95    | 0.95
_________________________________________________________________
> K-Nearest Neighbors |  86.8%     | 0.88      | 0.89    | 0.88
__________________________________________________________________
> Logistic Regression | 80.2%      | 0.82      |  0.83   |  0.82
__________________________________________________________________
> Naive Bayes         |  78.4%     |  0.82     |  0.79   |  0.80
 _________________________________________________________________

## 📌 Business Insights & Recommendations
The model's findings provide clear, data-driven recommendations for the airline:
- **Prioritize In-flight Experience**: Focus investments on improving Inflight wifi service, Inflight entertainment, and Seat comfort, as these are the strongest drivers of satisfaction.
- **Enhance Digital Service**s: The high importance of Online boarding suggests that a seamless digital experience is critical. Continue to invest in user-friendly booking and check-in platforms.
- **Address Economy Class Needs**: Given the significant satisfaction gap, conduct further research into the specific pain points of Economy and Economy Plus passengers to develop targeted service improvements.
- **Minimize Delays**: Punctuality is crucial. Efforts to reduce departure and arrival delays will have a direct positive impact on passenger satisfaction.

## 🛠️ Technologies Used
- Programming Language: Python
- Data Manipulation & Analysis: Pandas, NumPy
- Data Visualization: Matplotlib, Seaborn
- Machine Learning: Scikit-learn
- Development Environment: Jupyter Notebook

