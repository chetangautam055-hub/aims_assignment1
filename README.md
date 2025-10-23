# aims_assignment1
#Q1 ordinal_encoding.py

import pandas as pd

# Sample DataFrame
data = {
    'Size': ['Small', 'Medium', 'Large', 'Medium', 'Small']
}
df = pd.DataFrame(data)
print("Original Data:")
print(df)

#manual ordinal mapping
size_mapping = {'Small': 1, 'Medium': 2, 'Large': 3}

# Apply mapping
df['Size_Encoded'] = df['Size'].map(size_mapping)

print("\nAfter Ordinal Encoding:")
print(df)


#Q2
# one hot encoding

import pandas as pd

# Sample DataFrame
data = {
    'Color': ['Red', 'Blue', 'Green', 'Blue', 'Red']
}
df = pd.DataFrame(data)
print("Original Data:")
print(df)

# Perform One Hot Encoding 
df_encoded = pd.get_dummies(df, columns=['Color'])

print("\nAfter One Hot Encoding:")
print(df_encoded)





#Q3 imputation techniques
# imputation_techniques.py

import pandas as pd
import numpy as np
data = {
    'Age': [25, np.nan, 30, 22, np.nan],
    'Salary': [50000, 54000, np.nan, 48000, 52000]
}
df = pd.DataFrame(data)
print("Original Data with Missing Values:")
print(df)

# Technique 1: Fill missing values with mean
df['Age'] = df['Age'].fillna(df['Age'].mean())

# Technique 2: Fill missing values with median
df['Salary'] = df['Salary'].fillna(df['Salary'].median())

print("\nAfter Imputation:")
print(df)
