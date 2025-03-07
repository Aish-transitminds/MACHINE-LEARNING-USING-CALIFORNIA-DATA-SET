# MACHINE-LEARNING-USING-CALIFORNIA-DATA-SET
Here’s the step-by-step explanation of your Python code without stars in the font:  

---

### Step 1: Import Required Libraries  
The first step is importing necessary libraries:  
- `pandas` for handling the dataset  
- `matplotlib.pyplot` for data visualization  
- `seaborn` for enhanced visualizations  

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

---

### Step 2: Load the Dataset  
The dataset is read from a CSV file (`california_housing.csv`) using `pandas.read_csv()`.  
This assumes that the file is in the same directory as your script.  

```python
df = pd.read_csv("california_housing.csv")
```

---

### Step 3: Display Dataset Information  
- `df.info()` provides an overview of the dataset, including column names, data types, and non-null values.  
- `df.head()` displays the first 5 rows to get a quick look at the data.  

```python
print("Dataset Overview:")
print(df.info())

print("\nFirst 5 Rows:")
print(df.head())
```

---

### Step 4: Compute the Correlation Matrix  
- `df.corr()` calculates the correlation matrix, which helps in understanding relationships between numerical features.  

```python
correlation_matrix = df.corr()
```

---

### Step 5: Visualize the Correlation Matrix using a Heatmap  
- The `sns.heatmap()` function is used to create a heatmap visualization of the correlation matrix.  
- `annot=True` ensures that values are displayed inside each cell.  
- `cmap='coolwarm'` defines the color scheme.  
- `fmt=".2f"` ensures that numbers are formatted to 2 decimal places.  
- `linewidths=0.5` provides separation between cells for better readability.  

```python
plt.figure(figsize=(10, 6))  # Set figure size
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f", linewidths=0.5)
plt.title("Correlation Matrix Heatmap")
plt.show()
```

---

### Step 6: Create a Pair Plot  
- `sns.pairplot()` is used to visualize pairwise relationships between numerical features in the dataset.  
- `diag_kind='kde'` specifies that kernel density estimation (KDE) plots should be used for diagonal elements.  

```python
sns.pairplot(df, diag_kind='kde')
plt.show()
```

---

### Final Output  
1. Dataset Overview: Displays dataset information (column names, data types, missing values, etc.).  
2. First 5 Rows: Prints a preview of the dataset.  
3. Correlation Matrix Heatmap: A heatmap showing correlations between numerical features.  
4. Pair Plot: A grid of scatter plots and KDE plots to explore feature relationships.  
