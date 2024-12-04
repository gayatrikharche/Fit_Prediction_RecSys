# Fit Prediction for Rent the Runway Data

This project focuses on building a personalized recommendation system for **Rent the Runway**, leveraging machine learning techniques to enhance customer experience. The system predicts the suitability of rented clothing items based on user demographics, rental history, physical attributes, and rental context.

## Project Overview

The primary goal of this project is to design and evaluate models that can predict the *fit feedback* for clothing rentals, offering precise recommendations for size, style, and fit. The project also addresses challenges like class imbalance and explores various machine learning models, from simple classifiers to advanced neural networks.

### Key Features
- **Exploratory Data Analysis (EDA):** Uncovered patterns and relationships in user reviews, rental preferences, and fit feedback.
- **Machine Learning Models:** Implemented multiple models, including:
  - Logistic Regression
  - Support Vector Machines (SVM)
  - k-Nearest Neighbors (k-NN)
  - Gradient Boosting Models (XGBoost, CatBoost)
  - Neural Networks (Text Mining-CNN, TabNet, Multilayer Perceptron)
- **Balancing Techniques:** Addressed class imbalance using downsampling, oversampling, and evaluation metrics like balanced F2-scores.
- **Evaluation Metrics:** Used accuracy, precision, recall, and F2-scores to assess model performance, with a focus on optimizing recall to minimize false negatives.

### Dataset
The dataset includes user reviews, demographics, rental history, physical attributes, and rental context. Preprocessing steps included:
- Feature standardization and encoding
- Handling missing values
- Balancing minority classes

## Results
The **Text Mining-CNN Model** outperformed all other models, achieving:
- **Accuracy:** 0.8232
- **Unbalanced F2-score:** 0.8151
- **Balanced F2-scores:** 
  - 0.7030 (downsampling)
  - 0.8467 (oversampling)

## Models and Performance

Several models were evaluated based on accuracy, unbalanced F2-score, and balanced F2-score after applying downsampling and oversampling techniques. Below is a summary of the best-performing models:

### Model Performance:
Here's the table formatted in markdown for your README file:


# Model Performance Comparison across Different Sampling Methods

| Model                                | Accuracy | Unbalanced 𝐹𝛽 | Balanced 𝐹𝛽 (DS) | Balanced 𝐹𝛽 (OS) |
|--------------------------------------|----------|----------------|-------------------|-------------------|
| **Random Guessing:**                 |          |                |                   |                   |
| Uniform Random Guessing              | 0.3346   | 0.3447         | 0.3254            | 0.3293            |
| Weighted Random Guessing             | 0.5767   | 0.5765         | 0.3269            | 0.3350            |
| **Naïve Bayes (Gaussian):**          | 0.7351   | 0.6857         | 0.2564            | 0.2980            |
| **Logistic Regression Models:**      |          |                |                   |                   |
| Using All Features                   | 0.7339   | 0.6853         | 0.4503            | 0.4485            |
| Using Top 5 Features (RFE)           | 0.7340   | 0.6854         | 0.4470            | 0.4486            |
| Using Body-Related Features          | 0.7339   | 0.6854         | 0.4420            | 0.4406            |
| **Distance-Based Models k-NN:**      |          |                |                   |                   |
| Using All Features                   | 0.7081   | 0.6749         | 0.3925            | 0.3962            |
| Using Body-Related Features          | 0.7086   | 0.6771         | 0.4064            | 0.4066            |
| **SGD-Based SVM:**                   | 0.7351   | 0.6857         | 0.4202            | 0.4116            |
| **Matrix Factorization Latent Factor Model:** | 0.7350 | 0.6856 | 0.3916            | 0.3892            |
| **Gradient Boosting Models XGBoost:**| 0.7353   | 0.6865         | 0.4647            | 0.4554            |
| **CatBoost Classifier**              | 0.7356   | 0.6872         | 0.4620            | 0.4644            |
| **Random Forest:**                   | 0.7360   | 0.6873         | 0.4585            | 0.4546            |
| **Single Decision Tree:**            | 0.7332   | 0.6877         | 0.4549            | 0.4453            |
| **Multilayer Perceptron**            | 0.7352   | 0.6859         | 0.4108            | 0.4531            |
| **Ensemble learning**                | 0.7343   | 0.6858         | 0.4527            | 0.4524            |
| **TabNet**                            | 0.7351   | 0.6857         | 0.3050            | 0.4539            |
| **Bayesian Personalized Ranking (BPR)** | 0.3532 | 0.7207         | 0.7000            | 0.6800            |
| **Text Mining-CNN Model:**           | 0.8232   | 0.8151         | 0.7030            | 0.8467            |

### Key Observations:
- **Best Performing Model:** The Text Mining-CNN model demonstrated superior performance across all evaluation metrics.
- **Balancing Effect:** Advanced models like CNN and XGBoost showed improvements with oversampling, while simpler models showed performance drops.
- **Baselines:** The uniform random guessing model performed poorly across all metrics, serving as a baseline for comparison.

## Conclusion

The fit prediction task presented a challenging multiclass classification problem, requiring effective model selection, feature engineering, and balancing techniques. The Text Mining-CNN model emerged as the best-performing model for this task, demonstrating the effectiveness of deep learning in tackling complex, imbalanced datasets.

## Future Work

- **SMOTE (Synthetic Minority Over-sampling Technique):** Explore the use of SMOTE for further improvement in handling class imbalance.
- **Precision-Recall Curves:** Use more advanced metrics like precision-recall curves to evaluate the model's performance on minority classes.

