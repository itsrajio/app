import pandas as pd
import numpy as np

# Create a Series
ser = pd.Series([10, 20, 30, 40, 50])
print("Series:")
print(ser)

# Create a Series with custom index
ser_custom = pd.Series([10, 20, 30, 40, 50],
                       index=['a', 'b', 'c', 'd', 'e'])
print("\nCustom Series:")
print(ser_custom)

# Create a DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Department': ['HR', 'IT', 'HR', 'IT'],
    'Age': [24, 27, 22, 25],
    'Salary': [50000, 60000, 52000, 58000]
}

df = pd.DataFrame(data)
print("\nDataFrame:")
print(df)

# Selecting columns
print("\nName Column:")
print(df['Name'])

# Selecting rows
print("\nFirst Row:")
print(df.iloc[0])

# Data Cleaning
df.loc[1, 'Age'] = np.nan
print("\nMissing Values:")
print(df.isnull())

df['Age'] = df['Age'].fillna(df['Age'].mean())
print("\nAfter Filling Missing Values:")
print(df)

# Grouping and Aggregation
print("\nAverage Salary by Department:")
print(df.groupby('Department')['Salary'].mean())

print("\nSalary Statistics:")
print(df.groupby('Department')['Salary'].agg(
    ['mean', 'sum', 'max']
))
