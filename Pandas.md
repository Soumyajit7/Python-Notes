# Pandas

```python
pip install pandas
```

### 1. Importing Pandas
```python
import pandas as pd
```

### 2. Creating DataFrames
You can create a DataFrame from a dictionary, list, or another DataFrame.
```python
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 35]}
df = pd.DataFrame(data)
print(df)
```

### 3. Reading Data
You can read data from various file formats like CSV, Excel, SQL, etc.
```python
df = pd.read_csv('data.csv')
df = pd.read_excel('data.xlsx')
```

### 4. Viewing Data
You can view the first few rows, last few rows, or a summary of the DataFrame.
```python
print(df.head())  # First 5 rows
print(df.tail())  # Last 5 rows
print(df.info())  # Summary
print(df.describe())  # Statistical summary
```

### 5. Selecting Data
You can select columns, rows, or specific elements.
```python
print(df['Name'])  # Select a column
print(df[['Name', 'Age']])  # Select multiple columns
print(df.iloc[0])  # Select the first row
print(df.loc[0, 'Name'])  # Select a specific element
```

### 6. Filtering Data
You can filter data based on conditions.
```python
print(df[df['Age'] > 30])  # Filter rows where Age > 30
```

### 7. Adding/Removing Columns
You can add or remove columns in a DataFrame.
```python
df['Salary'] = [50000, 60000, 70000]  # Add a new column
df.drop('Salary', axis=1, inplace=True)  # Remove a column
```

### 8. Handling Missing Data
You can handle missing data by filling or dropping them.
```python
df.fillna(0, inplace=True)  # Fill missing values with 0
df.dropna(inplace=True)  # Drop rows with missing values
```

### 9. Grouping Data
You can group data and perform aggregate functions.
```python
grouped = df.groupby('Age').sum()
print(grouped)
```

### 10. Merging/Joining DataFrames
You can merge or join DataFrames.
```python
df1 = pd.DataFrame({'ID': [1, 2, 3], 'Name': ['Alice', 'Bob', 'Charlie']})
df2 = pd.DataFrame({'ID': [1, 2, 4], 'Age': [25, 30, 40]})
merged_df = pd.merge(df1, df2, on='ID', how='inner')
print(merged_df)
```

### 11. Sorting Data
You can sort data by values or index.
```python
df.sort_values(by='Age', ascending=False, inplace=True)  # Sort by Age
df.sort_index(inplace=True)  # Sort by index
```

### 12. Applying Functions
You can apply functions to DataFrame elements.
```python
df['Age'] = df['Age'].apply(lambda x: x + 1)  # Increment Age by 1
```

### 13. Pivot Tables
You can create pivot tables for summarizing data.
```python
pivot_table = df.pivot_table(values='Age', index='Name', aggfunc='mean')
print(pivot_table)
```

### 14. Exporting Data
You can export data to various file formats.
```python
df.to_csv('output.csv', index=False)
df.to_excel('output.xlsx', index=False)
```
