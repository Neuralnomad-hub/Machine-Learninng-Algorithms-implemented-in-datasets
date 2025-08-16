🌲 Forest Cover Type Prediction using Environmental & Geographic Data
📌 Problem Statement

The goal of this project is to predict the forest cover type (tree species/ecosystem) of a 30×30 meter plot of forest land using environmental and geographic features such as elevation, slope, soil type, and distance to hydrology/roads/fire points.

This is a multiclass classification task with 7 forest cover types:

1 → Spruce/Fir
2 → Lodgepole Pine
3 → Ponderosa Pine
4 → Cottonwood/Willow
5 → Aspen
6 → Douglas-fir
7 → Krummholz

👉 Business Value: Accurate cover type prediction supports forest management, wildfire risk assessment, ecological conservation, and land-use planning.

📂 Dataset

Source: Scikit-learn’s fetch_covtype (US Forest Service survey data)

Shape: 581,012 rows × 55 columns

Target Variable: Cover_Type (7 classes)

🔑 Key Features

Elevation (meters)

Aspect (azimuth angle in degrees)

Slope (degree incline)

Horizontal/Vertical Distance to Hydrology

Horizontal Distance to Roadways / Fire Points

Hillshade indices (9am, Noon, 3pm)

Wilderness Areas (4 binary flags)

Soil Types (40 binary indicators)

📊 Sample Rows
Elevation	Aspect	Slope	Horz_Dist_Hydro	Vert_Dist_Hydro	Horz_Dist_Road	Hillshade_Noon	Soil_Type_2	Soil_Type_12	Cover_Type
2596	51	3	258	0	510	232	0	0	5
2590	56	2	212	-6	390	235	0	0	5
2804	139	9	268	65	3180	238	0	0	2
🧹 Data Preparation

Handled 581k rows with no missing values

Feature Encoding: Soil types (40 binary columns), Wilderness areas (4 binary flags)

Train-Test Split: 80% train / 20% test

Feature Scaling: Not required for tree-based models

🔎 Exploratory Data Analysis (EDA)

Elevation strongly differentiates between cover types

Wilderness Areas and Soil Types provide categorical separation

Distances to Hydrology, Roads, Fire Points influence species distribution

Class distribution is imbalanced: Cover Types 1 & 2 dominate

🤖 Machine Learning Model

Model Used: RandomForestClassifier (ensemble learning)

Reason: Handles non-linear relationships, high-dimensional data, and categorical features efficiently

Hyperparameter Search: GridSearchCV (initial defaults shown, tunable for optimization)

from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)

📈 Results
🏆 Model Performance (on Test Data)
Class (Cover Type)	Precision	Recall	F1-Score	Support
1 → Spruce/Fir	0.96	0.94	0.95	42,557
2 → Lodgepole Pine	0.95	0.97	0.96	56,500
3 → Ponderosa Pine	0.94	0.97	0.96	7,121
4 → Cottonwood/Willow	0.91	0.84	0.88	526
5 → Aspen	0.94	0.77	0.85	1,995
6 → Douglas-fir	0.94	0.90	0.92	3,489
7 → Krummholz	0.97	0.95	0.96	4,015

Overall Accuracy: 95%
Macro Avg F1-Score: 0.92
Weighted Avg F1-Score: 0.95

✅ Insight: Random Forest effectively models the ecological complexity of forest cover types. Performance is strongest on dominant classes (1 & 2), while rarer classes (4, 5) show lower recall, suggesting potential for further tuning or class balancing.

🚀 Next Steps

Hyperparameter tuning with RandomizedSearchCV

Try advanced models: XGBoost, LightGBM, CatBoost

Class rebalancing using SMOTE / Class Weights

Feature importance analysis & visualization

🛠️ Tech Stack

Language: Python 🐍

Libraries: scikit-learn, pandas, matplotlib

ML Paradigm: Supervised Learning → Classification

Algorithm: Random Forest Classifier (Ensemble Learning)

📌 Key Takeaways

Solved a real-world ecological problem with high accuracy

Demonstrated strong skills in data wrangling, EDA, and ML model development

Delivered a scalable, interpretable model for forest management applications

✨ This project highlights expertise in large-scale data handling, feature engineering, and applied machine learning for environmental science — making it a strong portfolio piece for Data Science & AI roles.
