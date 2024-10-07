# Predicting-Mobile-Plan-Selection-for-Megaline---Project-7

## Project Overview

Megaline, a major mobile carrier, aims to optimize its customer service by recommending new mobile plans to users currently on legacy plans. The goal of this project is to develop a machine learning model that can predict which of Megaline's two modern plans—**Smart** or **Ultra**—a customer is most likely to choose based on their usage behavior.

### Key Features:
- **Calls**: Number of calls made and total call duration per month.
- **Messages**: Number of text messages sent per month.
- **Data Usage**: Internet data usage per month.
- **Target**: The mobile plan a customer chose—**Smart** (0) or **Ultra** (1).

### Objectives:
1. **Data Preprocessing**: Clean and preprocess the data to prepare it for machine learning.
2. **Model Training**: Train and validate multiple models to classify which plan a customer would select.
3. **Evaluation**: Compare the performance of models and select the best-performing one.

## Project Structure

The project includes the following main components:

- **Data Preprocessing**: This step involves handling missing values, outlier detection, feature engineering, and preparing the data for training.
- **Modeling**: Multiple models are trained, including decision trees, random forests, and gradient boosting classifiers.
- **Evaluation**: The models are evaluated using accuracy, precision, recall, and F1 score to ensure robust predictions.

## Notebooks

The project is organized in Jupyter notebooks, where each notebook represents a specific step of the project pipeline:

- **01_data_preprocessing.ipynb**: Contains all data preprocessing steps including cleaning, feature transformation, and splitting the dataset into training, validation, and test sets.
- **02_model_training.ipynb**: In this notebook, different models are trained and validated on the processed dataset.
- **03_evaluation.ipynb**: This notebook focuses on evaluating and comparing the performance of different machine learning models using several metrics.

## Results

After evaluating different models, the final model with the highest performance was chosen based on its ability to predict customer plan selection with an F1 score of **XX** (replace with actual score).

## Dependencies

This project is built using Python and the following libraries:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

You can install the dependencies using the following command:

```bash
pip install -r requirements.txt
