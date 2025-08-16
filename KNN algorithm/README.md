🐟 Fish Species Classification using KNN
📌 Problem Statement

The goal of this project is to classify different fish species based on their physical measurements such as weight, length, height, and width. Accurate classification helps in fisheries management, ecology research, and sustainable practices.

📂 Dataset

Source: Fish dataset (commonly used in ML classification tasks).

Features:

Weight, Length1, Length2, Length3, Height, Width

Target:

Species (Bream, Perch, Roach, Smelt, Parkki, etc.)

Sample (first 5 rows):

Species	Weight	Length1	Length2	Length3	Height	Width
Bream	242.0	23.2	25.4	30.0	11.52	4.02
Bream	290.0	24.0	26.3	31.2	12.48	4.31
Bream	340.0	23.9	26.5	31.1	12.38	4.70
Bream	363.0	26.3	29.0	33.5	12.73	4.46
Bream	430.0	26.5	29.0	34.0	12.44	5.13
🔎 Data Exploration & Visualization

Plotted scatter plots between species vs. weight to check class distribution.

Observed distinct clusters for different fish species.

⚙️ Machine Learning Model

Algorithm Used: K-Nearest Neighbors (KNN)

Reason: Simple, effective, non-parametric model suitable for classification with small datasets.

Steps:

Split dataset into training (80%) and testing (20%).

Trained KNN with k=3 neighbors.

Tested on unseen data.

📊 Results

Achieved good accuracy in classifying multiple fish species.

Sample Predictions:

['Perch', 'Smelt', 'Parkki', 'Perch', 'Bream', 'Roach']


Example test case (new fish with custom dimensions):

Input: Weight=234, Length1=234, Length2=234, Length3=234, Height=234, Width=234  
Prediction: ['Bream']

💡 Key Insights

KNN works well for this dataset due to clear separation in feature space.

Weight, Length, and Height are strong predictors of species.

Model can be extended with other classifiers (Random Forest, SVM, Neural Networks) for comparison.

🚀 Skills Highlighted

Data Preprocessing & Cleaning

Exploratory Data Analysis (EDA)

Supervised Machine Learning (KNN Classifier)

Evaluation & Prediction
