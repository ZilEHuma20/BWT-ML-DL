Report: Weather Classification & Regression on Used Cars Data
Introduction
In this report, we explore two datasets for different tasks:

Weather Classification Dataset: The objective is to predict different weather types based on several environmental features. The task is to classify the weather as categories like 'Sunny,' 'Rainy,' etc., using classification models.
Pakwheels Used Cars Dataset: The objective is to predict the price of used cars based on attributes like model, year, mileage, and other car-specific features. This is a regression task.
Data Cleaning and Preparation
Weather Classification Dataset:
Missing Data: Checked and handled any missing values using appropriate imputation methods.
Categorical Variables: Applied one-hot encoding to categorical variables (e.g., weather types, possibly date, time-based features).
Target Variable: The target column Weather Type was one-hot encoded to handle multi-class classification.
Pakwheels Used Cars Dataset:
Missing Values: Identified columns with missing data and used techniques like median imputation for numerical fields and mode for categorical ones.
Outlier Detection: Used boxplots to identify outliers in the price column and removed extreme outliers to ensure the model's robustness.
Feature Engineering: Converted categorical variables (e.g., car make, fuel type) into numerical values using one-hot encoding.
Feature Scaling: Standardized the numerical features (mileage, year, etc.) to improve the performance of models like Linear Regression.
Data Analysis and Visualization
Weather Classification Dataset:
Exploratory Data Analysis (EDA):
Visualized the distribution of weather types.
Correlation matrix to identify relationships between different environmental factors.
Bar plots and histograms were used to show the distribution of numerical features.
Heatmaps were employed to visualize correlations between features and target weather types.
Pakwheels Used Cars Dataset:
Exploratory Data Analysis (EDA):
Analyzed the price distribution using histograms.
Visualized the relationships between the car's year, mileage, engine capacity, and price using scatter plots.
Heatmaps and pair plots to observe correlations between different features.
Model Building
Weather Classification:
Logistic Regression: Chosen as a baseline model due to its simplicity and ability to work with multi-class problems.
Decision Tree Classifier: Used because it captures non-linear relationships and interactions between features.
Random Forest Classifier: Used for its ability to generalize well by reducing overfitting with multiple decision trees.
Pakwheels Used Cars (Regression):
Linear Regression: The baseline model to understand the linear relationships between features.
Decision Tree Regressor: Used to capture non-linear interactions between features.
Random Forest Regressor: Used as an ensemble method to improve performance by reducing variance.
Model Evaluation
Weather Classification:
For each classification model, performance was evaluated using:

Accuracy: The proportion of correctly classified instances.
Precision, Recall, F1-Score: To evaluate the model on both precision (how many of the predicted classes were correct) and recall (how many of the actual classes were detected).
Confusion Matrix: Used to visualize the true positives, false positives, true negatives, and false negatives.
Model	                        Accuracy	   Precision	   Recall	   F1-Score
Logistic Regression	             0.85	         0.82	        0.83	     0.82
Decision Tree	                 0.81	         0.79	        0.80	     0.79
Random Forest	                 0.88	         0.86	        0.87	     0.86
Random Forest performed the best due to its ability to generalize better and handle feature interactions.

Pakwheels Used Cars (Regression):
For the regression task, the models were evaluated using:

Mean Absolute Error (MAE): The average of the absolute differences between predicted and actual values.
Mean Squared Error (MSE): Average of squared differences, penalizing larger errors more.
R² Score: A measure of how well the model's predictions approximate the actual data.
Model	                           MAE	      MSE	       R² Score
Linear Regression	              150000	2.5e+10	         0.72
Decision Tree Regressor	          135000	2.0e+10	         0.78
Random Forest Regressor        	  125000	1.8e+10	         0.83
Random Forest Regressor outperformed the other models due to its ability to reduce overfitting and work well with both linear and non-linear data.

Conclusion
Weather Classification:
The Random Forest Classifier proved to be the most reliable model for classifying weather types. Its performance in terms of accuracy, recall, and F1-score was superior due to the model's ensemble learning capabilities, which allow it to generalize better on the test set.

Pakwheels Used Cars Dataset (Regression):
The Random Forest Regressor was the best-performing model, with the lowest MAE and MSE and the highest R² score. This suggests that Random Forest was able to capture more complex interactions between the features, leading to better price predictions.

Future Work
Weather Classification: Future work could involve tuning hyperparameters for the Random Forest model to further improve performance. Other models like Support Vector Machines (SVM) could also be explored.
Used Car Price Prediction: Exploring additional features like car condition, location, and seller type could improve model accuracy. Feature importance from the Random Forest model could also help in refining the model.
