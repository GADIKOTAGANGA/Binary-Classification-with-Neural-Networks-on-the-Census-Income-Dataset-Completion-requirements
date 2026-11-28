# Binary-Classification-with-Neural-Networks-on-the-Census-Income-Dataset-Completion-requirements
AIM

To develop a binary classification model using PyTorch to predict whether an individual's annual income is greater than $50,000 or less than or equal to $50,000 using the Census Income Dataset.

OBJECTIVES
To load and understand the Census Income Dataset.
To separate categorical, continuous and label columns.
To preprocess the dataset and handle missing values.
To convert data into PyTorch tensors.
To design a neural network using PyTorch.
To train the model using Adam optimizer.
To evaluate the model using test loss and accuracy.
SOFTWARE REQUIREMENTS
Operating System: Windows 11
Programming Language: Python
IDE: Visual Studio Code
Framework: PyTorch
Libraries: NumPy, Pandas, Scikit-learn
Notebook: Jupyter Notebook
DATASET DESCRIPTION
Dataset Name: Census Income Dataset
File Name: income.csv
Total Records: 30,000
Target Column: label
Class 0: Income less than or equal to $50,000
Class 1: Income greater than $50,000
PROCEDURE
Import the required libraries.
Set random seed for reproducibility.
Load the Census Income Dataset.
Separate categorical, continuous and label columns.
Handle missing values.
Encode categorical features.
Create arrays and tensors.
Split data into training and testing sets.
Define the TabularModel class.
Initialize loss function and optimizer.
Train the model for 300 epochs.
Evaluate test loss and accuracy.
Predict income for new user inputs.

Program
```
import os
import pandas as pd
from pathlib import Path
possible_paths = [
    Path("../income.csv"),
    Path("income.csv"),
    Path("../Census-Income-Classification/income.csv"),
    Path.cwd() / "income.csv",
    Path.home() / "Downloads" / "income.csv"
]
csv_path = next((path for path in possible_paths if path.exists()), None)
if csv_path is None:
    raise FileNotFoundError("income.csv not found. Please place it in the project folder or Downloads folder.")
df = pd.read_csv(csv_path)
df.columns = df.columns.str.strip()
print("Dataset Loaded Successfully!")
print("Dataset Location:", csv_path.resolve())
print("Dataset Shape:", df.shape)
print("\nFirst 5 Records:")
print(df.head())
print("\nDataset Columns:")
print(df.columns.tolist())
```
Output

<img width="1058" height="377" alt="Screenshot 2026-11-28 082440" src="https://github.com/user-attachments/assets/4461ce7a-48c6-4ebc-a4e1-c04d106f4072" />

Result


Thus, the Census Income Classification project was successfully implemented and executed using Python and PyTorch. The neural network model was trained for 300 epochs and successfully performed binary classification to predict whether an individual's annual income is greater than $50,000 or less than or equal to $50,000.

The program executed successfully and produced the test loss, test accuracy, and income prediction results.Census Income Classification Using PyTorch
