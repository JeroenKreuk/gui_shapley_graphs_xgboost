# Shapely Graphs + XGBoost Auto Tuner

This Python script provides a Graphical User Interface (GUI) for performing various operations related to Shapley values and XGBoost model tuning. It incorporates functionalities such as data preprocessing, feature importance analysis, feature selection, SMOTE resampling, XGBoost hyperparameter optimization using Optuna, and SHAP (SHapley Additive exPlanations) plots.

## Usage
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/fc902231-0d9f-4067-b80c-3210c1548a9c)

1. **Run the Script:**
   Execute the script to launch the GUI.

2. **Open Database:**
   Click the "Open Database" button to choose a CSV file. The script reads the data and allows further processing.

3. **Data Processing:**
   - Use the listbox to select the target/label column.
   - Click the "Process" button in the "Dummies" section to perform quick data processing, including random sampling and one-hot encoding.

4. **Feature Importance:**
   - Click the "Process" button in the "Feature Importance" section to calculate and display feature importances using a RandomForestRegressor.
   - Specify an importance threshold in the "Feature Selection" section.

5. **Feature Selection:**
   - Click the "Process" button in the "Feature Selection" section to filter features based on the specified importance threshold.
   - Checkboxes for scaling and SMOTE options are available.

6. **SMOTE & Scaling:**
   - Click the "Process" button in the "SMOTE & Scaling" section to apply SMOTE and scaling to the selected features.

7. **XGBoost Hyperparameters:**
   - Optuna is used for hyperparameter optimization. Click the "Process & Show Results" button in the "Hyperparameters" section.
   - The best hyperparameters will be displayed, and the XGBoost model will be trained.

8. **Results:**
   - Cross-validation scores, mean cross-validation score, train score, and test score will be printed in the console and displayed in the "Results" section.
   - Feature importance is also shown.

9. **Shapley Graphs:**
   - Adjust settings in the "Shapley Graphs" section, including the number of individual and combined plots.
   - Check the desired Shapley graph types.
   - Click the "Waterfall," "Force," "Mean," "Beeswarm," "Violin," "Layered Violin," "Correlation Matrix Features," and "Shapley Correlation" checkboxes to generate corresponding SHAP plots.

↓Waterfall plot shows a single observation/instance and how each feauture of this single observation has contributed to the model prediction.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/78331b7f-1df5-4107-b7b3-ec785a3f9e64)
↓Force plot is similar to the waterfall plot only displayed differently.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/6ca930f8-d542-4db9-96cb-1ecdb21f1855)
↓Mean SHAP plot visualize the absolute mean SHAP value across all instances.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/fd76aea1-a278-4a2b-b6be-d9a7d4d021cd)
↓Beeswarm visualises all of the SHAP values.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/c4c40218-d3fa-44c1-ab4f-2384390b511b)

↓Violin plot visualises all of the SHAP values.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/f4fb2e29-e98f-4824-9464-ea0675cc5510)
↓Layered violin plot visualises all of the SHAP values.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/3cc9fe29-ca7e-4b3a-8964-2286a38101a9)
↓Correraltion matrix, how the features are correlated to each other.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/73d815df-2d6d-4e01-9179-58009f67e4e1)
↓Shap value correraltion matrix, how the shap values are correlated to each other.
![image](https://github.com/JeroenKreuk/gui_shapley_graphs_xgboost/assets/85551796/f7ab740f-4c42-4c5a-9eb4-5e7c27c4f2cd)

## Dependencies

- Python 3.x
- Required Python libraries (install via `pip install <library>`):
  - numpy
  - tkinter
  - pandas
  - scikit-learn
  - imbalanced-learn
  - optuna
  - xgboost
  - shap
  - seaborn
  - matplotlib

## Note

- Ensure that you have the necessary dependencies installed before running the script.

Feel free to customize and extend the script based on your specific use case and requirements.

