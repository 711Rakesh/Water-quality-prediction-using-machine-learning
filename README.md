# Water-quality-prediction-using-machine-learning

This project focuses on predicting water potability using machine learning techniques. The dataset includes various water quality parameters, and the goal is to determine whether the water is safe for human consumption (Potable - 1) or not (Not potable - 0).

# Dataset
The dataset used in this project is available in kaggle. The features include pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic_carbon, Trihalomethanes, Turbidity, and the target variable Potability.
# Feature Description:
ph: pH of water (0 to 14).
Hardness: Capacity of water to precipitate soap in mg/L.
Solids: Total dissolved solids in ppm.
Chloramines: Amount of Chloramines in ppm.
Sulfate: Amount of Sulfates dissolved in mg/L.
Conductivity:Electrical conductivity of water in μS/cm.
Organic_carbon: Amount of organic carbon in ppm.
Trihalomethanes:Amount of Trihalomethanes in μg/L.
Turbidity: Measure of light emitting property of water in NTU.
Potability: Indicates if water is safe for human consumption (Potable - 1, Not potable - 0).

# Exploratory Data Analysis

Data Cleaning: Handling missing values by replacing them with the mean of the respective columns.
Skewness Analysis: Checking the skewness of features, excluding the target variable.
Outlier Detection: Utilizing box plots to identify potential outliers.

# Data Visualization

Histogram Plots: Visualizing the distribution of different features.
Count Plot: Analyzing the count of potable and non-potable water samples.
Correlation Plot: Understanding the correlation between different features.
Scatter Plot: Examining the relationship between pH and potability.

# Model Training
Partitioning: Splitting the dataset into training and testing sets.
Random Forest Classifier: Utilizing the Random Forest model for prediction.

# Model Evaluation
Accuracy Score: Assessing the accuracy of the model, achieving approximately 69%.

# Additional Metrics
Calculating additional metrics such as Precision, Recall, and F1 Score to provide a more comprehensive evaluation of the model.
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score

# Calculating metrics
accuracy_score_rf = accuracy_score(y_test, pred_rf)
precision_rf = precision_score(y_test, pred_rf)
recall_rf = recall_score(y_test, pred_rf)
f1_rf = f1_score(y_test, pred_rf)

print(f"Accuracy: {accuracy_score_rf*100:.2f}%")
print(f"Precision: {precision_rf:.2f}")
print(f"Recall: {recall_rf:.2f}")
print(f"F1 Score: {f1_rf:.2f}")

# Plotting the metrics
metrics = ['Accuracy', 'Precision', 'Recall', 'F1 Score']
values = [accuracy_score_rf, precision_rf, recall_rf, f1_rf]

plt.figure(figsize=(10, 6))
sns.barplot(x=metrics, y=values, palette='viridis')
plt.title('Model Metrics')
plt.show()
```

These metrics provide a more detailed understanding of the model's performance beyond accuracy.

Conclusion:
This water quality prediction model aims to contribute to sustainable water resource management. Continuous refinement and optimization can further enhance the model's accuracy and reliability.
