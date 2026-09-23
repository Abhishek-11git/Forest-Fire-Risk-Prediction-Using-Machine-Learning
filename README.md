# Forest Fire Risk Prediction Using Machine Learning

## Overview

This mini project predicts whether weather and fire-weather conditions indicate **Fire** or **Not Fire**. It is an educational binary-classification project based on historical Algerian forest-fire observations.

The notebook covers data loading, preprocessing, exploratory analysis, model training, model comparison, evaluation, and an interactive prediction interface.

## Objective

Build a model that receives weather and fire-weather values and returns:

- **High Fire Risk** or **Low Fire Risk**
- Estimated probability of fire

## Dataset

| Item | Details |
| --- | --- |
| Name | [The extended Algerian forest fires dataset](https://data.mendeley.com/datasets/8rkd9cdgs5/1) |
| Source file | `The extended Algerian forest fires dataset.csv` |
| Raw records | 1,215 |
| Target | `Classes` (`fire` or `not fire`) |
| Final encoded target | `Fire` (`1 = Fire`, `0 = Not Fire`) |

Place the downloaded CSV file in the **same folder** as the notebook before running it.

## Features Used by the Final Model

| Feature | Meaning |
| --- | --- |
| Temperature | Temperature in degrees Celsius |
| RH | Relative humidity percentage |
| Ws | Wind speed in kilometres per hour |
| Rain | Rainfall in millimetres |
| FFMC | Fine Fuel Moisture Code |
| DMC | Duff Moisture Code |
| ISI | Initial Spread Index |

## Technologies and Libraries

- Python 3.11
- Jupyter Notebook
- Pandas and NumPy for data preparation
- Matplotlib and Seaborn for visualization
- Scikit-learn for machine learning
- Joblib for model serialization
- Ipywidgets for the interactive notebook interface

## Installation

1. Install Python 3.11 and Jupyter Notebook.
2. Download this project and the dataset CSV file.
3. Open a terminal in the project folder.
4. Install the required packages:

```bash
pip install -r requirements.txt
```

5. Start Jupyter Notebook:

```bash
jupyter notebook
```

6. Open `AbhishekBabajiSangamnere_ForestFirePrediction.ipynb`.
7. Choose **Run All Cells**.

## Project Workflow

```text
Dataset CSV
    -> Data cleaning and preprocessing
    -> Exploratory data analysis
    -> Feature selection
    -> Train test split and scaling
    -> Model training and comparison
    -> Random Forest selection
    -> Interactive fire-risk prediction
```

## Models Compared

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

The dataset is split into 80% training data and 20% testing data. The final model is selected using accuracy, precision, recall, and F1-score.

## Result

Random Forest is selected as the final model. On the held-out test data, it achieved approximately:

| Metric | Result |
| --- | ---: |
| Accuracy | 91% |
| Fire Precision | 93% |
| Fire Recall | 90% |
| Fire F1-score | 91% |

## Using the Prediction Interface

After running every notebook cell, enter values for Temperature, Relative Humidity, Wind Speed, Rainfall, FFMC, DMC, and ISI. Click **Predict Fire Risk** to see the predicted class and fire probability.

## Project Files

```text
AbhishekBabajiSangamnere_ForestFirePrediction.ipynb       Main project notebook
requirements.txt                          Version-pinned Python dependencies
README.md                                 Project documentation
AbhishekBabajiSangamnere_ForestFirePredictionReport.docx Project report
The extended Algerian forest fires dataset.csv Dataset download
```

## Limitations

This model is intended for learning and project demonstration. It estimates risk from historical data; it is not a real-time emergency-warning system and must not be used for public-safety decisions.

## Reference

Abid, F. *The extended Algerian forest fires dataset*. Mendeley Data. https://data.mendeley.com/datasets/8rkd9cdgs5/1
