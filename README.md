# Encoder
# Categorical Feature Encoding Techniques

This repository contains a Jupyter Notebook (`Encode.ipynb`) that demonstrates various techniques for encoding categorical features in a dataset. Understanding and applying appropriate encoding methods are crucial steps in preparing data for machine learning models, as most models require numerical input.

## Table of Contents

  - [Project Overview](https://github.com/nouninasion/Encoder/blob/main/README.md#project-overview)
  - [Encoding Techniques Demonstrated](https://github.com/nouninasion/Encoder/blob/main/README.md#encoding-techniques-demonstrated)
      - [LabelEncoder](https://github.com/nouninasion/Encoder/blob/main/README.md#labelencoder)
      - [OrdinalEncoder](https://github.com/nouninasion/Encoder/blob/main/README.md#ordinalencoder)
      - [OneHotEncoder](https://github.com/nouninasion/Encoder/blob/main/README.md#onehotencoder)
      - [Mapping (Manual Encoding)](https://github.com/nouninasion/Encoder/blob/main/README.md#mapping-manual-encoding)
  - [Getting Started](https://github.com/nouninasion/Encoder/blob/main/README.md#getting-started)
  - [Libraries Used](https://github.com/nouninasion/Encoder/blob/main/README.md#libraries-used)

## Project Overview

This project provides practical examples of different categorical encoding techniques using the `scikit-learn` library and `pandas` for data manipulation. It covers scenarios where categorical data needs to be converted into a numerical format suitable for machine learning algorithms.

## Encoding Techniques Demonstrated

The notebook showcases the following encoding methods:

### LabelEncoder

`LabelEncoder` is used to transform non-numerical labels to numerical labels (0 to `n_classes`-1). This encoder should be used when there is no ordinal relationship between categories.

**Example from Notebook:**
Categories `['Asik', 'Baik', 'Nakal']` are encoded as follows:

  - `Asik`: 0
  - `Baik`: 1
  - `Nakal`: 2

### OrdinalEncoder

`OrdinalEncoder` transforms categorical features to ordinal integers. This is suitable when categories have a meaningful order (e.g., 'Good', 'Better', 'Best'). The order of categories can be explicitly defined.

**Example from Notebook:**
Categories `[['Asik', 'Baik', 'Nakal']]` are encoded as follows, based on the provided order:

  - `Asik`: 0.0
  - `Baik`: 1.0
  - `Nakal`: 2.0

### OneHotEncoder

`OneHotEncoder` is used to convert categorical variables into a one-hot numerical array. This method creates a new binary column for each category, where a '1' indicates the presence of that category and '0' indicates its absence. This is ideal for nominal (unordered) categorical data to prevent the model from assuming an ordinal relationship.

**Example from Notebook:**
The 'Condition' column with values `['Poor', 'Fair', 'Good', 'Excellent']` is converted into separate columns: `Condition_Excellent`, `Condition_Fair`, `Condition_Good`, `Condition_Poor`.

### Mapping (Manual Encoding)

This section demonstrates a simple, manual mapping approach using `pandas.DataFrame.map()` for binary categorical variables. This is useful when you have a clear, direct mapping of categories to numerical values (e.g., 'Yes' to 1, 'No' to 0).

**Example from Notebook:**
The 'Garage' column with `['Yes', 'No']` values is mapped to `1` and `0` respectively:

  - `Yes`: 1
  - `No`: 0

## Getting Started

To run this notebook, you will need Jupyter Notebook or Google Colab and the following libraries installed:

  - `pandas`
  - `scikit-learn`

You can install these using pip:

```bash
pip install pandas scikit-learn
```

Once the dependencies are installed, you can open and run the `Encode.ipynb` file in your Jupyter environment or Google Colab.

## Libraries Used

  - `pandas`
  - `sklearn.preprocessing`
