# House Price Prediction using MLflow

This project demonstrates how to use **MLflow** for tracking machine learning experiments. A simple Linear Regression model is trained on a house price dataset, and key parameters, metrics, and artifacts are logged using MLflow.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Setup Instructions](#setup-instructions)
3. [Steps to Run the Project](#steps-to-run-the-project)
4. [Using MLflow UI](#using-mlflow-ui)
5. [Understanding MLflow Functionalities](#understanding-mlflow-functionalities)
6. [Project Structure](#project-structure)
7. [Conclusion](#conclusion)

---

## Project Overview

**Objective:** Train a Linear Regression model to predict house prices and showcase the usage of **MLflow** to track experiments effectively.

**Key Highlights:**
- Logging model parameters, metrics (MSE, R² score), and trained model artifacts.
- Using MLflow's local UI to compare multiple runs and analyze performance.

---

## Setup Instructions

Follow the steps below to set up and run the project:

1. **Create a Virtual Environment**
   - You can create a virtual environment using conda with Python 3.10:
     ```bash
     conda create -n housing_venv python=3.10
     conda activate housing_venv
     ```

2. **Project Directory**
   - Create a folder to store the project files. For example:
     ```bash
     mkdir housing_prediction
     cd housing_prediction
     ```

3. **Install Requirements**
   - Add the required library to `requirements.txt`:
     ```
     mlflow
     ```
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```

4. **Run the Notebook**
   - Open the project folder in **Visual Studio Code**.
   - Activate the virtual environment in the terminal:
     ```bash
     conda activate housing_venv
     ```
   - Open the Jupyter Notebook file `house_predict_updated.ipynb`.

5. **Start MLflow UI**
   - In the terminal, start the MLflow UI:
     ```bash
     mlflow ui
     ```
   - This will provide a localhost address (e.g., `http://127.0.0.1:5000`), where you can view the MLflow UI.

6. **Run the Notebook Cells**
   - Execute the notebook cells one by one.
   - After the final cell is executed, all model parameters, metrics, and artifacts will be logged to MLflow.

7. **View Experiment Tracking**
   - Open the MLflow UI at `http://127.0.0.1:5000`.
   - Compare runs, analyze metrics, and view model artifacts.

---

## Using MLflow UI

After running the notebook and starting the MLflow UI:
1. **Navigate to the MLflow UI**: Visit `http://127.0.0.1:5000` in your browser.
2. **View Experiments**: All experiment runs will be listed with:
   - Parameters (e.g., model type)
   - Metrics (e.g., MSE, R² score)
   - Artifacts (e.g., trained model)
3. **Compare Runs**:
   - Select multiple runs to compare performance metrics.
   - Analyze improvements by tuning hyperparameters or changing the model.
4. **Download Artifacts**:
   - You can download the saved model or any other logged artifacts.

---

## Understanding MLflow Functionalities

MLflow is a powerful tool for managing the machine learning lifecycle. Here are some core functionalities showcased in this project:

### 1. **Experiment Tracking**
- Log parameters, metrics, and artifacts for each run.
- Compare different runs to identify the best-performing model.

### 2. **Model Logging**
- Use `mlflow.sklearn.log_model()` to log a trained scikit-learn model as an artifact.
- Easily load and use the logged model for predictions later.

### 3. **Metrics and Parameters Logging**
- Log custom metrics such as Mean Squared Error (MSE) and R² score using `mlflow.log_metric()`.
- Log model-specific parameters using `mlflow.log_param()`.

### 4. **Reproducibility**
- MLflow ensures that experiments are reproducible by storing parameters, code, and models.

### 5. **UI for Visualization**
- MLflow UI provides an easy-to-use interface to track experiments, compare runs, and download artifacts.

---

## Project Structure

The project directory is organized as follows:
```
project_folder/
|
|-- house_predict_updated.ipynb   # Main Jupyter Notebook for the project
|-- requirements.txt              # File containing project dependencies
|
|-- mlruns/                       # Auto-generated folder where MLflow logs are stored
```

---

## Conclusion

This project demonstrates how to effectively use MLflow for experiment tracking in a machine learning workflow. By logging parameters, metrics, and models, you can easily compare and reproduce results.

### Possible Extensions:
- Use a different model (e.g., Random Forest, XGBoost) and log results.
- Add hyperparameter tuning with libraries like `GridSearchCV`.
- Deploy the trained model using MLflow's model serving capabilities.

---

Happy Experimenting with MLflow! 🚀
