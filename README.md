## Vehicle Sales and Market Trends: Exploratory Data Analysis

This project performs an Exploratory Data Analysis (EDA) on a comprehensive dataset of vehicle sales transactions. The objective is to clean, transform, analyze, and visualize the data to derive actionable insights into market trends and pricing.

### Dataset Overview

The dataset includes details such as `year`, `make`, `model`, `trim`, `body type`, `transmission type`, `VIN`, `state of registration`, `condition rating`, `odometer reading`, `exterior and interior colors`, `seller information`, `Manheim Market Report (MMR)` values, `selling prices`, and `sale dates`.

### Key Analysis Steps:

1.  **Data Loading and Initial Inspection**: Loaded data from `car_prices.csv` and inspected its structure, types, and summary statistics.
2.  **Data Cleaning**: Dropped the unique `VIN` column, handled missing values by dropping rows, and standardized the `body` column casing.
3.  **Outlier Detection and Removal**: Identified and removed outliers in `sellingprice` using the Interquartile Range (IQR) method to ensure robust analysis.
4.  **Univariate Analysis**: Explored distributions of key variables like `year`, `transmission`, `make`, and `body type`.
5.  **Correlation Analysis**: Examined relationships between numerical features such as `year`, `condition`, `odometer`, `mmr`, and `sellingprice`.
6.  **Feature Addition**: Created a new feature, `price_diff` (sellingprice - mmr), to analyze the deviation from market value.

### Key Insights:

*   Newer vehicles dominate the used car market, with sales significantly increasing since the 2010s.
*   Automatic transmission vehicles are overwhelmingly more common than manual transmissions, a consistent trend across all states.
*   Ford and Chevrolet hold the largest market share among manufacturers, followed by Japanese and Korean brands.
*   Sedans and SUVs are the most prevalent body types in the dataset.
*   `MMR` and `sellingprice` show a very strong positive correlation, indicating `MMR` is a key predictor of sale price.
*   `Odometer` has a strong negative correlation with `sellingprice`, as expected.
*   The `price_diff` distribution shows that most cars sell at or slightly below their `MMR`, with some vehicles selling significantly above market value.

### Conclusion:

This EDA provides a solid foundation for understanding the vehicle sales market, highlighting significant factors influencing pricing and market share. The cleaned and transformed dataset, including the new `price_diff` feature, is now ready for further analysis.
