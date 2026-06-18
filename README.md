# 🛍️ Mall Customer Data Analysis

This project analyzes customer data from a shopping mall using **Python**. It includes correlation analysis, data distribution exploration, and data visualization using **Pandas**, **Matplotlib**, **Seaborn**, and **SciPy**.

---

## 📁 Dataset

The dataset used in this project is **Mall_Customers.csv**, which contains information about 200 customers with the following features:

| Column | Description |
|--------|-------------|
| `CustomerID` | Unique customer identifier |
| `Genre` | Gender of the customer |
| `Age` | Age of the customer |
| `Annual Income (k$)` | Annual income in thousands of dollars |
| `Spending Score (1-100)` | Score assigned by the mall based on customer behavior and spending nature |

---

## 📊 Analysis Performed

### 1. Data Exploration
- Displayed first 5 rows of the dataset (`head()`)
- Checked data types and missing values using `info()` and `isna()`

### 2. Pearson Correlation Coefficient

Using the `pearsonr` function from SciPy, correlation between the following feature pairs was calculated:

| Feature Pair | Correlation Coefficient | p-value |
|--------------|-------------------------|---------|
| Age & Annual Income | -0.0124 | 0.8617 |
| Age & Spending Score | -0.3272 | ≈ 0.000002 |
| Annual Income & Spending Score | 0.0099 | 0.8893 |

> **Key Insight:**  
> The only statistically significant correlation (p-value < 0.05) is between **Age** and **Spending Score**, showing a weak negative correlation.  
> Age and Income, as well as Income and Spending Score, show no significant linear relationship.

### 3. Visualizations

The following plots were created:

- 📈 **Scatter Plots** for each feature pair with correlation coefficients displayed on the plot
- 📊 **Boxplot** to compare income distribution across genders
- 🔥 **Heatmap** to visualize the full correlation matrix of numerical features

---

## 🧰 Libraries Used

- `pandas` – Data manipulation and analysis
- `numpy` – Numerical computations
- `matplotlib.pyplot` – Basic plotting
- `seaborn` – Advanced statistical visualizations
- `scipy.stats.pearsonr` – Pearson correlation coefficient calculation

---

## 📌 How to Run

1. Make sure the dataset file `Mall_Customers.csv` is located in the same directory as the notebook.
2. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

3. Run the Jupyter Notebook or Google Colab file.

---

## 📈 Sample Outputs

### Correlation Matrix (Numerical Features):

|                     | CustomerID | Age  | Annual Income | Spending Score |
|---------------------|------------|------|---------------|----------------|
| CustomerID          | 1.00       | -0.03| 0.98          | 0.01           |
| Age                 | -0.03      | 1.00 | -0.01         | -0.33          |
| Annual Income (k$)  | 0.98       | -0.01| 1.00          | 0.01           |
| Spending Score      | 0.01       | -0.33| 0.01          | 1.00           |


---

## 📝 Author

Motahare Mortezaiee - motahareh.mortezaiee@mail.com 
Date: June 2026

---

## 📄 License

This project is for educational purposes only.
