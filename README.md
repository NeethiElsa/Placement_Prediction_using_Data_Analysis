# Placement_Prediction_using_Data_Analysis
This project aims to analyze placement data to identify key factors influencing students' employability. Through data analysis techniques, we will examine the impact of CGPA, gender, domain preferences, and company selection criteria on placement outcomes. The findings from this study can help students, institutions, and recruiters make informed decisions to improve placement success rates.
#### Dataset Description
The dataset contains 10,000 rows and 12 features. Below is a description of each column:
1. Student ID- Unique ID for each student
2. CGPA – CGPA of the student.
3. Internships – Number of internships done by the student.
4. Projects – Number of projects by the student.
5. Workshops/Certifications – Number of certifications done by person.
6. AptitudeTestScore – Aptitude score achieved by the student.
7. SoftSkillsRating – Rating that showcases how good the student is in soft skills.
8. ExtracurricularActivities – Whether the student has taken part in extracurricular activities or not(Yes/No).
9. PlacementTraining - Whether the student has taken part in placement training or not(Yes/No).
10. SSC_Marks – Marks scored by student for SSC.
11. HSC_Marks - Marks scored by student for HSC.
12. PlacementStatus – Whether student has got placed or not.
    
#### Dataset Preprocessing
Removed StudentID (identifier)
Categorical Encoding: OneHotEncoding (drop='first')
Binary Columns: Only imputation (no scaling)
Numeric Columns: Mean imputation + StandardScaler
Class Imbalance: SMOTE (Synthetic Minority Oversampling)

#### Models Tried
Logistic Regression
Decision Tree Classifier
Random Forest Classifier
KNN
Support Vector Machine
Gradient Boosting Classifier (Best performance)

#### Final Model: Gradient Boosting Classifier
Learning Rate: 0.2
Estimators: 200
Performance: ~85% test accuracy
Tuned using GridSearchCV with 5-fold cross-validation

### Evaluation Metrics
Accuracy
Precision / Recall
F1-Score
Confusion Matrix

#### Deployment Ready
Final pipeline is saved using joblib
Can load and predict on new data.

#### Conclusion
Gradient Boosting Classifier performed the best with an testing accuarcy of 81% among the 6 models.
The model was able to identify the 2 classes in the unseen data which shows its ability to distinguish between the classes.
The data was slightly imbalanced which was rectified with SMOTE technique.The data had no missing or null values.Additionally,Encoding and Scaling was applied to the data as well.
Hyperparameter tuning has helped to increase the testing accuracy of Gradient Boosting Classifier from 79% to 81% even it did not change the accuracies of the other models.

#### Future Work
Model Updates: Periodically update the model with new data to ensure it adapts to changing trends and behaviors over time.
Feature Engineering: Apply dimensionality reduction techniques like PCA if feature space becomes large.
Continous Monitoring: Track the real-world performance of the model after deployment using metrics like precision, recall, and F1-score.
Data Collection Improvement: Collect more data which might be predictive of placement.
