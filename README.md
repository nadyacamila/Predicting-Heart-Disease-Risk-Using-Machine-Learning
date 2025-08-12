# Predicting-Heart-Disease-Risk-Using-Machine-Learning

Heart disease has become one of the leading causes of deaths globally. Now with health data and machine learning (ML), we can now finally have a greater chance of being able to predict it long before it happens.  This project support the Sustainable Development Goal 3 (SDG 3) which is aiming at promoting healthy living and well-being of all people. The dataset is publicly available on Kaggle under a CC0 Public Domain license, meaning it can be used freely for research and education. The ain of this project is to create predictive models with the help of machine learning algorithms, such as Logistic Regression and XGBoost, which would be able to evaluate the risk of heart disease in a person based on the specified features.

# Preparation
- Not found any missing values, but found 1 duplicated value.
- Invalid values of Thal = 0 and CA = 4 was removed.
- Outliers was detected using **1.5×IQR rule, 3×IQR rule, and Z-Score.** But not removed due to it may represent actual extreme patient condition.
<img width="1203" height="629" alt="image" src="https://github.com/user-attachments/assets/8a1fe97b-8719-454d-8dd0-080ccd37cc2e" />
- The correlation of categorical/binary variables with target was analyze using point-biserial.

<img width="1279" height="962" alt="image" src="https://github.com/user-attachments/assets/fe87f228-8360-4bd9-96be-6f3dd11feb90" />
- Meanwhile, numerical correlation with target was analyze by Correlation Matrix Heatmap.
- **(+) correlation:** Higher feature values are linked with a **higher** chance of heart disease.
- **(-) correlation:** Higher feature values are linked with a **lower** chance of heart disease.
- **Key Insights:** - Thalassemia (Thal), Major Vessels (CA), Chest Pain Type (CP) is top predictor
                - Cholesterol & resting blood pressure showed weak correlation in this dataset.

# Modeling 
**Model**	                Accuracy	F1-Score	AUC   Feature Importance
**Logistic Regression**	  81.67%	  81.97%	 0.945  CA - CP - Sex
**XGBoost	  **            86.67%	  87.50%	 0.931  Thal_2 - CA - Thal_3

# Data Product
<img width="2579" height="993" alt="image" src="https://github.com/user-attachments/assets/6887529f-b233-48e0-b5c6-cc31c0faf948" />
- **Platform:** Google Colab + ipywidgets.
- **Function:** Users input health data via sliders/dropdowns → System returns risk prediction.
- **Use Cases:** Doctor decision support, self-assessment, rural health checks.


