# 🧠 Migraine Symptom Classifier

This project is a machine learning-based classification system to identify different types of migraines based on symptoms. It uses a Random Forest Classifier trained on symptom data to accurately categorize migraines into various clinical subtypes.

📂 Dataset
The dataset used is migraine_symptom_classification.csv, which contains features representing symptoms and a target column "Type" indicating the migraine category.
Target Classes
a. Basilar-type aura
b. Familial hemiplegic migraine
c. Migraine without aura
d. Other
e. Sporadic hemiplegic migraine
f. Typical aura with migraine
g. Typical aura without migraine

🔧 Features & Tools Used
1. Pandas for data manipulation
2. Scikit-learn for modeling, scaling, and evaluation
3. Random Forest Classifier with:
n_estimators=200
max_depth=12
random_state=42
4. StandardScaler for feature normalization

🚀 Workflow
1. Data Loading
Load CSV data into a Pandas DataFrame.
2. Feature Engineering
Separate features X and target y.
3. Train-Test Split
Split data using an 80-20 ratio, stratified to preserve class distribution.
4. Feature Scaling
Normalize input features using StandardScaler.
5. Model Training
Train a RandomForestClassifier on the scaled data.
6. Prediction & Evaluation
Make predictions on the test set and evaluate performance using:
-Accuracy Score
-Classification Report (precision, recall, F1-score)

📊 Results
The trained Random Forest Classifier achieved a commendable overall accuracy of 88.75% on the test dataset. A detailed classification report reveals that the model performs exceptionally well in identifying certain migraine types. For example, it achieved perfect precision and recall (1.00) for the class Typical aura without migraine, indicating flawless classification for this type. Similarly, it showed strong performance for Typical aura with migraine, with a precision of 0.92 and recall of 0.96, resulting in an F1-score of 0.94. For Migraine without aura, the model reached a perfect recall of 1.00 and an F1-score of 0.92. However, performance was less consistent for less-represented classes. For instance, Basilar-type aura had a precision of 0.50 and a recall of 0.25, and Sporadic hemiplegic migraine had perfect precision but a recall of only 0.67. The weighted average F1-score across all classes was 0.88, indicating that the classifier maintains high predictive power while handling class imbalance reasonably well. These results demonstrate the model’s strong potential for practical use, especially for the more common migraine subtypes.


📌 Notes
-Class imbalance might affect minority class performance (e.g., "Basilar-type aura").
-Further improvements may involve techniques like SMOTE for balancing or trying alternative models like XGBoost or SVM.

🧪 Future Improvements
-Incorporate more clinical data (age, triggers, frequency).
-Use deep learning for symptom-to-type mapping.
-Create a web interface for medical usage.
-Evaluate cross-validation for generalization.

