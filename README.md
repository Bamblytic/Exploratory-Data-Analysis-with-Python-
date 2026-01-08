
# Exploratory Data Analysis on Automobile Dataset

This project is a Jupyter notebook that performs **exploratory data analysis (EDA)** on a cleaned automobile dataset, focusing on understanding how technical specifications and categorical attributes relate to car prices and fuel consumption. [file:88]

The notebook builds on a pre‑processed version of the automobile dataset (with engineered features such as `city-L/100km` and `horsepower-binned`) and explores patterns, correlations, and group statistics. [file:88]

---

## Dataset

- Shape: **201 rows × 29 columns** after cleaning and feature engineering. [file:88]  
- Example features used in the analysis:  
  - Categorical: `make`, `aspiration`, `num-of-doors`, `body-style`, `drive-wheels`, `engine-location`, `engine-type`, `num-of-cylinders`, `fuel-system`, `horsepower-binned`, `diesel`, `gas`. [file:88]  
  - Numeric: `symboling`, `normalized-losses`, `wheel-base`, `length`, `width`, `height`, `curb-weight`, `engine-size`, `bore`, `stroke`, `compression-ratio`, `horsepower`, `peak-rpm`, `city-mpg`, `highway-mpg`, `price`, `city-L/100km`. [file:88]  

---

## Notebook overview

### 1. Initial inspection and summaries

- Loads the cleaned dataset and inspects the head, shape, and column names. [file:88]  
- Uses `describe()` on both numeric and categorical columns to summarize distributions, counts, unique values, and most frequent categories. [file:88]  

### 2. Univariate analysis

- Examines distributions of key numeric variables such as `price`, `engine-size`, `horsepower`, `city-mpg`, `highway-mpg`, and `city-L/100km`. [file:88]  
- Reviews categorical distributions with `value_counts()` for features like `drive-wheels`, `body-style`, `aspiration`, and `make` to understand class balance and dominant categories. [file:88]  

### 3. Bivariate analysis and correlation

- Computes a **correlation matrix** for numeric features including `wheel-base`, `length`, `width`, `curb-weight`, `engine-size`, `horsepower`, `city-mpg`, `highway-mpg`, `price`, and `city-L/100km`. [file:88]  
- Highlights strong relationships such as:  
  - High positive correlation between **engine-size and price**.  
  - Strong negative correlation between **fuel efficiency metrics (city/highway mpg) and price**.  
  - Strong positive correlation between **curb-weight and price**. [file:88]  

### 4. Grouping and pivot analysis

- Explores how **price varies by drive‑wheels** (`fwd`, `rwd`, `4wd`) using groupby and aggregation. [file:88]  
- Builds pivot tables of **average price by drive-wheels and body-style**, revealing that rear‑wheel drive (`rwd`) body styles tend to have higher average prices than front‑wheel drive (`fwd`) counterparts. [file:88]  
- Shows the distribution of vehicles across `drive-wheels` categories and their corresponding mean prices. [file:88]  

### 5. Categorical vs numeric relationships

- Investigates how `body-style` and `drive-wheels` jointly influence `price` through multi‑index groupby and pivot tables. [file:88]  
- Uses the `horsepower-binned` feature (`Low`, `Medium`, `High`) to relate power categories to other numeric attributes and price ranges, illustrating how higher horsepower bins align with higher prices. [file:88]  

---

## Key insights from the analysis

- **Vehicle size and weight** (wheel-base, length, width, curb-weight, engine-size) are strongly positively correlated with price, confirming that larger and more powerful cars tend to be more expensive. [file:88]  
- **Fuel efficiency** (city/highway mpg, city-L/100km) is strongly negatively correlated with price and positively correlated with engine size and horsepower, indicating a clear trade‑off between performance and efficiency. [file:88]  
- **Drive configuration and body style** matter: rear‑wheel drive sedans, hardtops, and convertibles generally occupy the higher price brackets, while front‑wheel drive hatchbacks and some wagons cluster at lower average prices. [file:88]  

---

## Technologies used

- Python  
- pandas for data manipulation, grouping, and summary statistics. [file:88]  
- NumPy for numerical computations. [file:88]  
- (Optionally) Matplotlib/Seaborn for visualizations, if plots were used during the analysis. [file:88]  
- Jupyter Notebook for interactive EDA. [file:88]  

