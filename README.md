# NDA Project: EDFA Power Prediction Using Neural Networks

This project focuses on predicting the output power of an Erbium-Doped Fiber Amplifier (EDFA) based on input parameters using a neural network model. The implementation is done in Python using TensorFlow and Scikit-learn, structured within a Jupyter notebook.

## 📁 Dataset

The dataset used is `Single_EDFA_Dataset.csv`. It contains experimental measurements for various EDFA input configurations.

- The target variable `measuredTotalPout` is dropped as part of preprocessing.
- Null values are checked and removed if present.

## 🔧 Main Features

### 1. Data Preprocessing
- Loads the dataset from a CSV file.
- Cleans and prepares the data by removing unnecessary columns and checking for missing values.
- Standardizes the input features using `StandardScaler`.

### 2. Data Splitting
- Splits the dataset into training and testing sets using `train_test_split`.
- Also utilizes K-Fold cross-validation for robustness.

### 3. Model Architecture
- Constructs a feedforward neural network using `TensorFlow` and `Keras`.
- A `Sequential` model is used with fully connected (`Dense`) layers.
- The model is wrapped in a `KerasRegressor` to integrate with Scikit-learn's tools.

### 4. Model Training & Evaluation
- The model is trained on the preprocessed dataset.
- Performance is evaluated using:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - R-squared score (R²)

### 5. Cross-Validation
- Performs K-Fold cross-validation to evaluate model stability and generalization.

## 🧠 Requirements

To run this notebook, make sure you have the following Python packages installed:

```bash
pip install numpy pandas scikit-learn matplotlib tensorflow scikeras
```

## 🚀 How to Run

1. Clone or download this repository.
2. Place the dataset `Single_EDFA_Dataset.csv` in the root directory.
3. Open the notebook `NDA_project_manual.ipynb` using Jupyter.
4. Run the cells sequentially.
