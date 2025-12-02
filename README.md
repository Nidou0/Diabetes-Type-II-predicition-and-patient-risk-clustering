End-to-end business intelligence & analytics pipeline for Glucowell Medical, a fictional specialized diabetes clinic, turning raw clinical records into diabetes risk predictions, patient risk clusters, and an interactive Power BI dashboard. 

BI_Assignement_report

What’s inside this repo:

🩺 Domain context – Glucowell Medical
Diabetes-focused clinic operating in a data-rich environment (clinical metrics, lifestyle factors, demographics) where decisions need to be evidence-based and patient-centric.

📊 Data & preprocessing (Python)

~211k patient records with 25 variables (BMI, blood pressure, fasting glucose, lipid profile, lifestyle & family history, etc.).

KNN imputation for missing clinical values, z-score normalization to align scales, and SMOTE to handle strong class imbalance in diabetes status.

Outlier detection via skewness/kurtosis, outlier counts, and boxplots for high-variance markers (e.g., triglycerides, ALT, AST).

🤖 Predictive modelling – Who is diabetic?
Three supervised models compared on precision, recall, and F1-score:

Logistic Regression – highly interpretable, very high recall but low precision (many false positives).

Support Vector Machine (SVM) – slightly better balance but still high false-positive rate.

Random Forest – best overall trade-off (Precision ≈ 0.883, Recall ≈ 0.822, F1 ≈ 0.852), making it the recommended model for Glucowell’s operational use.

🧩 Clustering for risk stratification

K-Means (k = 2) selected via Elbow Method and validated with Silhouette Score.

Patients grouped into high-risk vs low-risk diabetes clusters using clinically relevant features, forming the basis of a practical risk score for proactive follow-ups and early intervention.

📈 Power BI dashboard – From models to decisions

Interactive dashboard built on top of the cleaned & model-ready dataset (linked by PatientID).

DAX-engineered measures to track BMI, fasting glucose, lipid profiles, lifestyle habits, and cluster membership.

Highlights key insights: diabetes more prevalent in older patients, higher BMI, adverse lipid profiles, higher fasting glucose, and certain smoking categories.
