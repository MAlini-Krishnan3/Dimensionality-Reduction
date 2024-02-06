# Machine Learning Classification with Dimensionality Reduction

This project demonstrates a comprehensive approach to a classification task using a dataset with 168 features and 1 categorical target. The goal is to apply various dimensionality reduction techniques to improve model performance and compare the effectiveness of three different classification algorithms: Logistic Regression, Random Forest, and K-Nearest Neighbors (KNN).

## Dataset Overview

The dataset, `Feature_Target.xls`, contains 168 continuous features and 1 categorical target variable. The challenge involves preprocessing the dataset and applying dimensionality reduction techniques to optimize the feature space for classification.

## Dimensionality Reduction Techniques

The project employs four main strategies for feature selection and dimensionality reduction, applied in a chronological sequence:

1. **Variance Filter**: This method removes features with low variance, under the assumption that features with a low variance do not contribute much information for classification.

2. **Association Test**: Utilizes statistical tests (`f_classif` and `mutual_info_classif`) to select features with the highest association with the target variable.

3. **Recursive Feature Elimination (RFE)**: Iteratively constructs models and removes the weakest feature(s) until the specified number of features is reached.

4. **Principal Component Analysis (PCA)**: Reduces dimensionality by transforming features into a smaller number of uncorrelated components that capture the most variance in the data.

## Classification Algorithms

Three default classification models are evaluated:

- **Logistic Regression**
- **Random Forest**
- **K-Nearest Neighbors (KNN)**

Default models are used without specifying hyperparameters to maintain simplicity and focus on the impact of feature selection and dimensionality reduction.

## Experimental Conditions

Classification accuracy performances are compared under five data conditions:

1. **Raw unscaled data**: Baseline performance using the original dataset without any preprocessing.
2. **Scaled data**: Data normalized using Standard Scaler to standardize the feature set.
3. **Slightly reduced scaled data**: Data scaled and then reduced using variance filter and association tests for dimensionality reduction.
4. **Intermediately reduced scaled data**: Further reduction using association tests followed by RFE, including variance filtering.
5. **Highly reduced scaled data**: The most aggressive reduction applying association tests, RFE, and then PCA, including variance filtering.

## Evaluation and Visualization

The project evaluates the classification accuracy of each model under the five data conditions. A single grouped bar chart compiles the 15 classification accuracies (5 per technique) to visually compare the impact of each dimensionality reduction strategy on model performance.

## Implementation Details

The notebook is structured to ensure readability and understandability:

- **Comments and Text Cells**: Detailed explanations are provided throughout the notebook to describe the process, methodology, and decision-making at each step.
- **Code Organization**: The code is organized into sections corresponding to each stage of the process, from data loading and preprocessing to model training and evaluation.

This project aims to provide insights into how different dimensionality reduction techniques can affect the performance of classification algorithms and to determine the most effective approach for this specific dataset.
