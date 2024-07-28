# Age and Gender Data Analysis

This project provides scripts to analyze and visualize age and gender data from an Excel file (`ages_gender.xlsx`). The visualizations include bar charts and histograms for both age and gender distributions.

## Prerequisites

- Python 3.x
- pandas
- matplotlib
- openpyxl (if you're using pandas to read .xlsx files)

You can install the required packages using pip:

```sh
pip install pandas matplotlib openpyxl
```

**Data**

The data should be in an Excel file named ages_gender.xlsx with at least the following columns:

    Name: The name of the individual.
    Gender: The gender of the individual.
    Age: The age of the individual.
    Id: The age of the individual.

## Scripts

## Displaying Data

The following script loads the data and displays all rows and columns.

```sh 
import pandas as pd
filepath = "/home/rguktongole/Downloads/ages_gender.xlsx"
pd.set_option("display.max_rows", None)
pd.set_option("display.max_columns", None)
df = pd.read_excel(filepath)
print(df)
```

## Bar Chart for Gender Distribution

This script creates a bar chart showing the distribution of genders.
```sh
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel('/home/rguktongole/Downloads/ages_gender.xlsx')
gender_counts = df['Gender'].value_counts()
print(df[['Name', 'Gender']].head(10))
plt.bar(gender_counts.index, gender_counts.values, color='orange')
plt.xlabel('Gender')
plt.ylabel('Count')
plt.title('Distribution of Genders using Bar Charts')
plt.show()
```

## Bar Chart for Age Distribution

This script creates a bar chart showing the distribution of ages.

```sh
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel('/home/rguktongole/Downloads/ages_gender.xlsx')
age_counts = df['Age'].value_counts().sort_index()
print(df[['Name', 'Age']].head(10))
plt.bar(age_counts.index, age_counts.values, width=0.5, color='brown')
plt.xlabel('Ages')
plt.ylabel('Count')
plt.title('Distribution of Age using Bar Graph')
plt.show()
```
## Histogram for Age Distribution

This script creates a histogram showing the distribution of ages.
```sh
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel('/home/rguktongole/Downloads/ages_gender.xlsx')
print(df[['Name', 'Age']].head(10))
plt.hist(df['Age'], bins=5, color="green")
plt.xlabel('Ages')
plt.ylabel('Frequency')
plt.title('Distribution of Ages using Histogram')
plt.show()
```

## Histogram for Gender Distribution

This script creates a histogram showing the distribution of genders.

```sh
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel('/home/rguktongole/Downloads/ages_gender.xlsx')
print(df[['Name', 'Gender']].head(10))
plt.hist(df['Gender'], bins=2, color="purple")
plt.xlabel('Gender')
plt.ylabel('Frequency')
plt.title('Distribution of Genders using Histogram')
plt.show()
```

**Usage**

* Make sure your ages_gender.xlsx file is located in the specified path: /home/rguktongole/Downloads/ages_gender.xlsx.
* Run the scripts in your Python environment to generate the visualizations.

**License**

  This project is licensed under the MIT License. See the LICENSE file for details.

**Contact Information**

  For any queries or issues, please contact Latha at pulicheralalatha121@gmail.com








