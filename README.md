Georgia Real Estate Price Analysis
- An end-to-end machine learning project analyzing Georgia real estate listings to identify which property characteristics most significantly influence home sale prices.
- Tech Stack: Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn


- Problem Statement:

  - How do property characteristics combine to determine home sale prices in Georgia, and which factors are most influential?

- Dataset

  - Source: Georgia real estate listings, first half of 2021
  - Size: 13,804 rows × 39 columns
  - Key Features Used: livingArea, bathrooms, bedrooms, hasGarage, pool, homeType, county, isNewConstruction, yearBuilt


- Approach

  - Explored and cleaned a 39-column dataset, removing irrelevant identifiers, duplicate area columns, and highly corrupted records (e.g. properties listed with 89 bedrooms, year built values of 9999, and 4,000+ vacant lots)
  - Selected features most likely to influence price and engineered the final modeling dataset
  - Built and evaluated a Linear Regression model using Scikit-learn
  - Assessed performance using R², RMSE, and MAE, and checked for overfitting by comparing training vs. testing scores


- Results
  - Metric Value: R² Score 0.55
  - Mean Absolute Error: ~$84,480
  - RMSE: ~$117,500
  - Training vs. Testing R² gap: Minimal (no overfitting)

The model explains 55% of the variation in home prices
livingArea, bathrooms, and county were the most significant predictors of price
The low gap between training and testing R² indicates the model generalizes well and is not overfitting


- Limitations & Lessons Learned

  - The dataset was limited in scope — only covering Georgia listings from the first six months of 2021, which likely constrained the model's predictive power
  - Data quality issues required significant cleaning and may have impacted accuracy
  - Several potentially useful features (zipcode, buildingArea) were dropped early and may have contributed more than initially assumed
