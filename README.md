# Regression-Trees-on-TLC-Trip-Record-Data

# Regression Trees Analysis: Predicting Taxi Tips

This notebook demonstrates how to build and evaluate a regression tree model to predict taxi tip amounts using the NYC Taxi dataset. Below is a summary of the key steps and findings:

## Key Steps

1. **Data Preparation**:
   - Loaded the dataset containing taxi trip information
   - Examined correlations between features and the target variable (tip_amount)
   - Identified low-correlation features that could potentially be removed

2. **Model Training**:
   - Split data into training (70%) and testing (30%) sets
   - Built a Decision Tree Regressor with max_depth=8
   - Trained the model on the training data

3. **Evaluation**:
   - Evaluated model performance using MSE (Mean Squared Error) and R² score
   - MSE: 1.784
   - R²: 0.001 (very low, indicating poor predictive performance)

4. **Experimentation**:
   - Tested different max_depth values (4, 12)
   - Removed low-correlation features to simplify the model
   - Visualized the decision tree structure

## Key Findings

1. **Feature Importance**:
   - The top 3 features affecting tip amount are:
     1. fare_amount (highest correlation)
     2. tolls_amount
     3. trip_distance

2. **Model Performance**:
   - The initial model performed poorly (R² ≈ 0)
   - Reducing max_depth to 4 improved performance slightly
   - Increasing max_depth to 12 worsened performance (negative R²), indicating overfitting

3. **Feature Selection**:
   - Removing low-correlation features (payment_type, VendorID, etc.) had minimal impact on model performance
   - A simplified model using only the top 3 features performed similarly to the full-feature model
