Random Forest:

Data Preparation:

Datasets:
Campaign Performance Data: Used for training the model, includes historical CTR values and campaign features.
Submission Form Data: Contains new campaign details where CTR values need to be predicted.
Features:
Categorical Features: ad_file_type, ad_size, goal_type, media_type, campaign_type.
Numerical Features: goal_value, max_bid, plan_impressions, daily_impression_cap, daily_estimated_budget.
Preprocessing:

Categorical Variables:
Applied one-hot encoding to convert categorical features into numerical representations suitable for model training.
Numerical Variables:
Retained in their original form for modeling.
Combined all features into a unified dataset for training and prediction.
Model Development:

Algorithm Used: Random Forest Regressor.
Chosen for its robustness, ability to handle both categorical and numerical data, and resilience to overfitting.
Pipeline:
Integrated preprocessing steps and model training into a unified pipeline for streamlined execution.
Model Training:

Trained the Random Forest model on the labeled training dataset (campaign_performance.csv), using historical CTR as the target variable.
Prediction:

Predicted CTR values for the new campaigns provided in the test dataset (c2_submission_form.csv).
The predictions were added as a new column, predicted_ctr.
Output:

The updated dataset with predicted CTR values was saved as a new CSV file: c2_submission_form_with_predictions.csv.
Key Deliverables
Predicted CTR File:
c2_submission_form_with_predictions.csv containing new campaign data with predicted CTR values.

Random Forest R2 Score

Data Loading:

Two datasets were used:
Campaign Performance Data: Historical data containing features and CTR values for training.
Submission Form Data: New campaigns where CTR values need to be predicted.
Feature Engineering:

Categorical Features:
Included ad_file_type, ad_size, goal_type, media_type, campaign_type.
Preprocessed using one-hot encoding.
Numerical Features:
Included goal_value, max_bid, plan_impressions, daily_impression_cap, and daily_estimated_budget.
Modeling Pipeline:

Preprocessing:
Combined categorical and numerical preprocessing using a ColumnTransformer.
Model:
Random Forest Regressor was selected for its robustness, ability to handle non-linear relationships, and suitability for mixed data types.
Pipeline:
Integrated preprocessing and model training into a unified pipeline for efficiency and consistency.
Model Evaluation:

Cross-Validation:
Used 5-fold cross-validation to generate out-of-sample predictions for training data.
Metrics:
Calculated R² score on training data to measure how well the model explains CTR variability.
Example Result: R² Score: 0.8390.

Prediction:

The model predicted CTR values for new campaigns in the submission form data.
Predictions were added to the dataset as a new column: predicted_ctr.

Output:
The updated dataset was saved as c2_submission_form_with_predictionsr2.csv.

Key Results
R² Score: Provided a performance metric for how well the model fit the training data during cross-validation.

