# Tanzania-water-crisis
This repository contains a machine learning project that uses a dataset of water point functionality in Tanzania to predict which wells are in need of repair.

Machine Learning for Water Crisis: Identifying Non-Functional Wells in Tanzania


Business Problem:
The goal of this project is to locate wells in Tanzania that need repair in order to address the water crisis in the country. The dataset used is from the Taarifa waterpoints dashboard, which aggregates data from the Tanzania Ministry of Water. The main focus of this analysis is to maximize recall in order to identify non-functional wells that are most in need of repair, even if it means some functional wells are incorrectly labeled as non-functional.

Data Preparation and EDA:
Data cleaning was performed to eliminate non-factor columns, remove duplicates and null values, and categorize values in columns such as scheme_management and installer. Exploratory data analysis revealed that many regions have a higher proportion of non-functional waterpoints compared to functional waterpoints, highlighting the need for repairs and maintenance in those regions.

Modeling:
Baseline model was created using a dummy classifier model, which resulted in an accuracy score of 54%. Four other models were trained and evaluated, including Logistic Regression, Random Forest, XGBoost, and K Nearest Neighbors. Random Forest appeared to be the best choice among the evaluated models, as it achieved the highest accuracy, precision, recall, F1 score, and ROC AUC score. The top predictors of the Random Forest model were longitude, latitude, gps_height, age, and quantity_dry. An ensemble of the top-performing models might also be a good option to improve the robustness and generalization of the predictions.

Recommendations:
Based on the findings, stakeholders should focus on the location of the wells when making decisions on where to invest resources to improve functionality. This could involve targeting areas where toxic drainage systems are present and/or areas where wells are more likely to be non-functional due to their location. Additionally, wells that are older and have lower water quantity should be given priority for repair and maintenance to improve their functionality.

Limitations:
The models used in the analysis have limitations and may not capture the full complexity of the problem. There may also be other factors affecting the functionality of the wells that were not captured in the dataset.

Future Research:
Consider collecting additional data such as information on the maintenance history of waterpoints. Conducting surveys to gather more detailed information on the condition and use of waterpoints in various locations. Further research could be done to investigate the impact of other factors on the functionality of the wells, such as population density, the type of pump used, and the availability of maintenance resources.
