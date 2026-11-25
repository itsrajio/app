import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import zscore

# Sample Dataset
data = {
    'Age': [24, 27, 22, 32, 29, 25, 100],
    'Salary': [50000, 60000, 52000, 58000, 62000, 55000, 600000]
}

df = pd.DataFrame(data)

# Descriptive Statistics
print("Descriptive Statistics:")
print(df.describe())

print("\nMean:", df['Age'].mean())
print("Median:", df['Age'].median())
print("Mode:", df['Age'].mode()[0])
print("Standard Deviation:", df['Age'].std())
print("Variance:", df['Age'].var())
print("Minimum:", df['Age'].min())
print("Maximum:", df['Age'].max())

# Visualization
plt.hist(df['Age'], bins=5, edgecolor='black')
plt.title("Age Distribution")
plt.xlabel("Age")
plt.ylabel("Frequency")
plt.show()

sns.boxplot(y=df['Age'])
plt.title("Box Plot of Age")
plt.show()

plt.scatter(df['Age'], df['Salary'])
plt.title("Age vs Salary")
plt.xlabel("Age")
plt.ylabel("Salary")
plt.show()

sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.title("Correlation Matrix")
plt.show()

# Handling Missing Data
data_missing = {
    'Age': [24, 27, None, 32, 29, 25, None],
    'Salary': [50000, 60000, 52000, None, 62000, 55000, 60000]
}

df_missing = pd.DataFrame(data_missing)

print("\nMissing Values:")
print(df_missing.isnull())

print("\nAfter Removing Missing Values:")
print(df_missing.dropna())

print("\nAfter Filling Missing Values:")
print(df_missing.fillna(df_missing.mean()))

# Handling Outliers
df['Age_zscore'] = zscore(df['Age'])
df['Salary_zscore'] = zscore(df['Salary'])

print("\nZ-Scores:")
print(df)

df_no_outliers = df[
    (df['Age_zscore'].abs() <= 3) &
    (df['Salary_zscore'].abs() <= 3)
]

print("\nData After Removing Outliers:")
print(df_no_outliers)

# Capping Outliers
def cap_values(series):
    upper = series.mean() + 3 * series.std()
    lower = series.mean() - 3 * series.std()
    return series.clip(lower=lower, upper=upper)

df['Age_capped'] = cap_values(df['Age'])
df['Salary_capped'] = cap_values(df['Salary'])

print("\nCapped Values:")
print(df[['Age', 'Age_capped', 'Salary', 'Salary_capped']])
