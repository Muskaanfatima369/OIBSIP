Task 3 — Car Price Prediction with Machine Learning

Track: Data Science Program: Oasis InfoByte (OIBSIP)

Objective

Build a regression model that predicts the selling price of a used car based on features such as brand, age, mileage, fuel type, and transmission.

Dataset

"Vehicle dataset from cardekho" — sourced from Kaggle. Contains car name, manufacturing year, selling price, present (new) price, kilometers driven, fuel type, seller type, transmission, and ownership history.

Approach
Cleaned data: removed duplicates, handled nulls, standardized categorical text casing
Engineered features: Car_Age from Year, Brand extracted from car name
Explored price distribution, price by fuel type, and price vs. car age
One-Hot Encoded categorical variables (Fuel_Type, Seller_Type, Transmission)
Built a feature correlation heatmap
Split data 80/20 for train/test
Trained two regression models: Linear Regression and Random Forest Regressor
Evaluated both using MAE, RMSE, and R² score
Plotted feature importance for the best-performing model
Tech Stack

Python, pandas, scikit-learn, matplotlib, seaborn, Jupyter Notebook

Files
Car_Price_Prediction.ipynb — full notebook with code, explanations, and results
car_data.csv — dataset (note source here if excluded from the repo due to size/license)
Screenshots/outputs — to be added after running the notebook
Result
Model	MAE	RMSE	R²
Linear Regression	1.473	2.524	0.753
Random Forest	1.408	3.322	0.572

Best model: Linear Regression — despite Random Forest achieving a marginally lower MAE (1.408 vs 1.473), Linear Regression clearly wins on RMSE (2.524 vs 3.322) and R² (0.753 vs 0.572). The gap between Random Forest's MAE and RMSE performance indicates it is making a small number of large errors on the test set, consistent with overfitting — a common risk when training a flexible, unconstrained ensemble model (100 trees, no depth limit) on a small dataset (301 rows, ~240 used for training). Linear Regression's simpler structure generalizes better here, which lines up with the near-linear relationships already visible between Selling_Price and features like Present_Price and Car_Age in the correlation heatmap. Given the dataset size, this result should be read as specific to this data split — a larger dataset or a depth-limited/regularized Random Forest might close or reverse this gap.
