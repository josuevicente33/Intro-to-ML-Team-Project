# Intro-to-ML-Team-Project
README: Enhanced Preprocessed Dataset
Overview
This dataset is an enhanced and preprocessed version of the gym members' exercise tracking data. The preprocessing prepares the data for various machine learning tasks such as BMI risk classification, cardiovascular risk prediction, and activity level classification. This dataset is standardized, clean, and ready for use by all team members for their specific tasks.

Required Python Libraries
To run this preprocessing pipeline, ensure the following Python libraries are installed:
pip install pandas scikit-learn tabulate

Preprocessing Steps
Loading the Dataset:

The original raw dataset was loaded from gym_members_exercise_tracking.csv.
Handling Missing Values:

Numeric Features: Missing values were replaced with the median of the respective column.
Categorical Features: Missing values were replaced with the mode of the respective column.
Encoding Categorical Variables:

Gender was one-hot encoded into Gender_Male.
Workout_Type was one-hot encoded into categories like Workout_Type_HIIT and Workout_Type_Strength.
Feature Normalization:

Numerical features such as Age, Weight (kg), BMI, and Calories_Burned were normalized using StandardScaler to have a mean of 0 and a standard deviation of 1.
Feature Engineering:

Heart Rate Zone: Created a categorical feature dividing Max_BPM into:
Fat-Burning, Cardio, and Peak zones.
BMI Category: Created a categorical feature dividing BMI into:
Underweight, Normal, Overweight, and Obese.
Activity Score: A composite feature combining Workout_Frequency and Session_Duration to reflect overall activity.
Encoding Engineered Features:

Heart_Rate_Zone and BMI_Category were one-hot encoded for model compatibility.
Saving the Processed Dataset:

The final preprocessed dataset is saved as enhanced_processed_gym_data.csv.
Dataset Columns
The dataset includes:

Normalized Numerical Features:
Age, Weight (kg), Height (m), BMI, Max_BPM, Avg_BPM, Resting_BPM, Session_Duration (hours), Calories_Burned, Fat_Percentage, Water_Intake (liters), Workout_Frequency (days/week).
Categorical Features:
Gender_Male, Workout_Type_HIIT, Workout_Type_Strength, Workout_Type_Yoga.
Engineered Features:
Heart_Rate_Zone_Cardio, Heart_Rate_Zone_Peak, BMI_Category_Normal, BMI_Category_Overweight, BMI_Category_Obese, Activity_Score.
Usage Instructions
Accessing the Dataset:

Download the processed dataset from the file enhanced_processed_gym_data.csv.
For Each Task:

Select relevant columns for your specific classification task (e.g., BMI for BMI risk classification, Max_BPM for cardiovascular risk).
Add task-specific labels as needed (e.g., binary or multi-class labels).
Starting Model Development:

Use the dataset as input for training machine learning models.
Ensure task-specific preprocessing (e.g., label generation) is done if needed.
