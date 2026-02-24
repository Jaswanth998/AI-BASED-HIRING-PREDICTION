# AI-BASED-HIRING-PREDICTION
AI-Based Hiring Prediction is a machine learning project that predicts whether a candidate will be hired based on skills, education, and experience. It includes data preprocessing, exploratory data analysis, and model training using Python and Scikit-learn to support data-driven recruitment and improve hiring decision accuracy.

### AI-Based Hiring Prediction System ###

End-to-End Machine Learning Project


Project Objective

In this project, you will build an AI-based Hiring Prediction System using a resume screening dataset.

The goal is to develop a Machine Learning model that predicts whether a candidate will be:
• Hired (1)
• Rejected (0)

based on resume information such as skills, experience, education, certifications, projects, and salary expectations.

This project simulates a real-world AI resume screening system used in HR analytics.

⸻

Dataset Description

The dataset contains 1,000+ synthetic resumes with the following columns:
• Resume_ID – Unique identifier
• Name – Candidate name
• Skills – List of technical skills
• Experience (Years) – Total work experience
• Education – Highest qualification
• Certifications – Relevant certifications
• Job Role – Applied job role
• Recruiter Decision – Hire or Reject (Target Variable)
• Salary Expectation ($) – Expected salary
• Projects Count – Number of projects completed
• AI Score (0–100) – AI-based screening score

⸻

Important Instructions
• Target variable: Recruiter Decision
• Convert:
• Hire → 1
• Reject → 0
• Drop the following columns before training:
• Resume_ID
• Name
• Do NOT use AI Score as a feature if your goal is to simulate independent hiring prediction.

⸻

TASK 1: Load and Understand the Dataset

Perform the following:
1. Import required libraries:
• pandas
• numpy
• seaborn
• matplotlib
• sklearn
2. Load the dataset using pd.read_csv().
3. Display:
• First 5 rows
• Last 5 rows
• Random samples
4. Write a short explanation:
• What type of data is present?
• Which column will be used as the target?

⸻

TASK 2: Basic Data Inspection

Using code, answer:
• Number of rows and columns
• Column names
• Data types of each column
• Value counts of Recruiter Decision
• Summary statistics for numerical columns

Explain why data inspection is important before model training.

⸻

TASK 3: Data Cleaning and Preprocessing
1. Drop:
• Resume_ID
• Name
2. Convert Recruiter Decision:
• Hire → 1
• Reject → 0
3. Check for missing values.
• If present, explain how you would handle them.
4. Ensure numeric columns are correctly formatted.

⸻

TASK 4: Text Feature Engineering

The following columns contain text:
• Skills
• Certifications
• Job Role

Perform:
1. Combine them into one column:
combined_text
2. Clean the text:
• Convert to lowercase
• Remove special characters
• Remove extra spaces

Explain why text cleaning is necessary before vectorization.

⸻

TASK 5: Convert Text to Numerical Features

Use:
• TfidfVectorizer

Convert combined_text into numeric features.

Explain:
• Why ML models cannot work directly with text.
• What TF-IDF represents.

⸻

TASK 6: Encode Categorical Variables

Encode:
• Education

using:
• Label Encoding or One-Hot Encoding

Explain the difference between them.

⸻

TASK 7: Feature and Target Separation
1. Separate:
• Features (X)
• Target (y)
2. Explain why Recruiter Decision should not be included in X.

⸻

TASK 8: Train–Test Split

Split the dataset:
• 80% Training
• 20% Testing
• random_state = 42

Explain:
• Why train–test split is necessary
• What overfitting means

⸻

TASK 9: Feature Scaling

Apply StandardScaler to numerical features:
• Experience (Years)
• Salary Expectation
• Projects Count

Explain:
• Why scaling is important
• Which models require scaling

⸻

TASK 10: Model Training

Train at least four models:
1. Logistic Regression
2. Random Forest
3. Support Vector Machine
4. K-Nearest Neighbors

Use scaled/unscaled data appropriately.

Write a short explanation of how each model works.

⸻

TASK 11: Model Evaluation and Comparison
1. Print accuracy score for all models.
2. Display classification report.
3. Create a comparison table:

Model Name | Accuracy
4. Answer:
• Which model performed best?
• Why might it perform better on this dataset?

⸻

TASK 12: (Optional Advanced) Pipeline and GridSearch
1. Create a Pipeline using:
• TfidfVectorizer
• StandardScaler (for numeric features)
• Logistic Regression or SVM
2. Use GridSearchCV to tune:
• C parameter
• Kernel (for SVM)
3. Print:
• Best parameters
• Best cross-validation score

Explain why pipelines are used in production systems.

⸻

TASK 13: Build Hiring Prediction Function

Create a function that:
• Takes user input:
• Skills
• Experience
• Education
• Certifications
• Projects Count
• Salary Expectation
• Returns:
• Prediction (Hire or Reject)
• Probability score

This simulates a real AI resume screening tool.

⸻

TASK 14: Final Conclusion

Write a conclusion covering:
• Dataset understanding
• Key preprocessing steps
• Best performing model
• What you learned
• How this project connects to real-world HR automation
