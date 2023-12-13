## Perform a chi-square test of independence when the original column values violate the expected counts assumption

``` python
# import necessary packages
import pandas as pd
import scipy.stats as stats
from scipy.stats import chi2_contingency

# read in the data
df = pd.read_csv("Student Mental health.csv")

# view data
df.head()

# check expected counts assumption
df['What is your course?'].value_counts()

# edit the values of the course column to meet the expected counts assumption of the chi-square test
df['What is your course?'] = df['What is your course?'].where(df['What is your course?'].isin(['BCS', 'Engineering', 'BIT']), 'Other')

# Create a contingency table
contingency_table = pd.crosstab(df['What is your course?'], df['Do you have Depression?'])

# Perform the Chi-Squared test
chi2, p, dof, expected = chi2_contingency(contingency_table)

print("Chi-Squared value:", chi2)
print("p-value:", p)


```

