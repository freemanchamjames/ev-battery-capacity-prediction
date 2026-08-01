# EV Battery Capacity Prediction

Graduate coursework project comparing regression models for estimating electric-vehicle battery capacity from published vehicle specifications.

## Project Objective

The objective was to analyze the relationships among electric-vehicle characteristics and develop a regression model to estimate battery capacity in kilowatt-hours (kWh).

## Models Compared

The project evaluated:

* Linear Regression
* Random Forest Regressor
* XGBoost Regressor

The models were compared using R², Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).

## Workflow

The notebook includes:

* Data inspection and cleaning
* Exploratory data analysis
* Analysis of feature distributions and relationships
* Feature engineering
* Regression preprocessing pipelines
* Model training and comparison
* Hyperparameter tuning
* Test-set evaluation

## Results

XGBoost produced the strongest test-set performance:

* **R²:** 0.977
* **MAE:** 2.15 kWh
* **RMSE:** 2.93 kWh

The R² result indicates that the model explained approximately 97.7% of the variation in battery capacity within the test data. Its MAE indicates that predictions differed from the recorded battery capacity by approximately 2.15 kWh on average.

## Tools and Technologies

* Python
* pandas
* NumPy
* scikit-learn
* XGBoost
* Matplotlib
* Seaborn
* Google Colab

## Repository Contents

```text
ev-battery-capacity-prediction/
├── README.md
├── ev_battery_capacity_prediction.ipynb
└── .gitignore
```

## Running the Notebook

The notebook can be opened in Google Colab or run locally with Jupyter Notebook.

To install the required packages locally:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn jupyter
```

Then start Jupyter:

```bash
python -m notebook
```

Open `ev_battery_capacity_prediction.ipynb` and run the cells in order.

## Interpretation and Limitations

Battery capacity is closely related to vehicle range and energy consumption. Because these specifications were included as model features, the strong predictive performance is consistent with the underlying engineering relationship:

Battery capacity (kWh) ≈ Range (km) × Energy consumption (Wh/km) ÷ 1,000

The results demonstrate regression modeling and model comparison within the available dataset. They should not be interpreted as independent battery testing or predictions for vehicles outside the data represented.

## Intended Use

This repository documents a graduate data-science coursework project and demonstrates:

* Regression modeling
* Data cleaning and exploratory analysis
* Feature engineering
* Preprocessing pipelines
* Hyperparameter tuning
* Model evaluation and interpretation
