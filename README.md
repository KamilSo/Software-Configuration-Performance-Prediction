# Configuration Performance Learning

A Python-based machine learning tool for predicting software system performance from configuration parameters.

This project explores how different regression models can be used to estimate performance metrics such as runtime, latency, or throughput from software configuration data. It was developed as part of my Computer Science studies at the University of Birmingham.

## Overview

Modern software systems often have many configurable parameters, and different combinations can significantly affect performance.

This project applies machine learning techniques to configuration-performance datasets in order to:

- predict system performance from configuration values
- compare different regression approaches
- evaluate prediction accuracy using multiple error metrics
- repeat experiments across different train/test splits
- analyse and visualise model performance

The project currently compares:

- Linear Regression
- Random Forest Regression

# Running the Project
### 1. Clone the repository
```
git clone https://github.com/KamilSo/Configuration-Performance-Learning.git
cd Configuration-Performance-Learning/pythonProject2
```
### 2. Install dependencies
```
pip install pandas numpy scikit-learn matplotlib scipy
```
*Tkinter is included with most standard Python installations.*
### 3. Add datasets
Place compatible CSV datasets inside:

> pythonProject2/Datasets/

The datasets should contain:
- numerical software configuration features
- a target performance column such as:
  - time
  - runtime
  - latency
  - throughput
  - performance
  - execution_time
If none of these column names are found, the final column is used as the target.

### 4. Run the application
```
python RandomForestTool.py
```

## Features 

- Automatic CSV dataset loading
- Automatic detection of likely performance target columns
- Validation of input features
- Configurable train/test split
- Repeated experiments using different random seeds
- Comparison of multiple regression models
- Performance evaluation using:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Percentage Error (MAPE)
- Statistical comparison of model results
- Result visualisation using Matplotlib
- Graphical interface built with Tkinter
- Support for exporting experimental results

## Tech Stack

- Python
- pandas
- NumPy
- scikit-learn
- Matplotlib
- SciPy
- Tkinter

## Machine Learning Approach

For each dataset, the configuration parameters are treated as input features and the measured software performance is treated as the prediction target.

The tool:

1. Loads the dataset from CSV.
2. Identifies the target performance column.
3. Separates features and target values.
4. Splits the dataset into training and testing sets.
5. Trains each regression model.
6. Generates predictions on unseen test data.
7. Evaluates the predictions using MAE, RMSE, and MAPE.
8. Repeats the experiment using multiple random train/test splits.
9. Compares the results across models.

## Models

### Linear Regression

Linear Regression is used as a simple baseline model.

It assumes a linear relationship between software configuration parameters and the resulting performance.

### Random Forest Regression

Random Forest Regression is used to model more complex, non-linear relationships between configuration settings and performance.

The current implementation uses an ensemble of decision trees and supports parallel model training.

## Evaluation Metrics

### Mean Absolute Error

Measures the average absolute difference between predicted and actual values.

Lower values indicate better predictions.

### Root Mean Squared Error

Places greater emphasis on larger prediction errors.

This is useful for identifying models that occasionally produce particularly inaccurate predictions.

### Mean Absolute Percentage Error

Expresses prediction error as a percentage of the true value.

The implementation safely handles cases where target values may contain zeros.

## What I Learned
This project helped me develop practical experience with:
- supervised machine learning
- regression modelling
- model evaluation
- experimental methodology
- software performance prediction
- data preprocessing
- repeated train/test experimentation
- statistical comparison of model results
- Python scientific computing libraries
- building a desktop interface around a data-processing workflow
It also strengthened my understanding of the trade-offs between simple interpretable models and more flexible ensemble methods.

## Future Improvements
Possible extensions include:
- additional regression models
- hyperparameter optimisation
- cross-validation
- feature importance analysis
- support for categorical configuration parameters
- improved visualisations
- automated model selection
- command-line interface support
- support for larger datasets
- more detailed experiment reporting
  
Author
Kamil Sobolewski
MSci Computer Science student at the University of Birmingham
