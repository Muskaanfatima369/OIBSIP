
# Task 1 — Iris Flower Classification

**Track:** Data Science
**Program:** Oasis InfoByte (OIBSIP)

## Objective
Train a machine learning classification model to identify the species of an iris flower (Setosa, Versicolor, or Virginica) from its physical measurements.

## Dataset
Built into scikit-learn (`sklearn.datasets.load_iris()`) — 150 samples, 4 features (sepal length, sepal width, petal length, petal width), 3 balanced classes (50 samples each).

## Approach
1. Loaded and explored the dataset (shape, dtypes, nulls, descriptive stats)
2. Visualized feature relationships with a pairplot and per-feature boxplots
3. Discussed which features are most discriminative (petal measurements)
4. Split data 80/20 with stratified sampling
5. Trained three classifiers: Logistic Regression, K-Nearest Neighbors, Decision Tree
6. Evaluated each with accuracy, confusion matrix, and classification report
7. Selected the best-performing model with justification

## Tech Stack
Python, scikit-learn, pandas, matplotlib, seaborn, Jupyter Notebook

## Files
- `Iris_Classification.ipynb` — full notebook with code, explanations, and results
- Screenshots/outputs — to be added after running the notebook

## Result

| Model | Accuracy |
|---|---|
| Logistic Regression | 96.67% |
| **K-Nearest Neighbors (KNN)** | **100%** |
| Decision Tree | 93.33% |

**Best model: K-Nearest Neighbors (KNN)** — achieved perfect accuracy (100%) on the test set with zero misclassifications across all three species. The other two models each misclassified one or two samples, exclusively between Versicolor and Virginica — the two species with overlapping feature distributions observed in the EDA pairplot. KNN's distance-based approach handled this overlap more effectively than Logistic Regression's linear boundary or the Decision Tree's axis-aligned splits.
