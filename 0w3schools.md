# Pandas 
- Pandas is a Python library.
- Pandas is used to analyze data.
## What is Pandas?
- Pandas is a Python library used for working with data sets.
- It has functions for analyzing, cleaning, exploring, and manipulating data.
- The name "Pandas" has a reference to both "Panel Data", and "Python Data Analysis" and was created by Wes McKinney in 2008.
## Why use Pandas?
- Pandas allows us to analyze big data and make conclusions based on statistical theories.
- Pandas can clean messy data sets, and make them readable and relevant.
- Relevant data is very important in data science.
### Note: Data Science: is a branch of computer science where we study how to store, use and analyze data for deriving information from it.
## What can Pandas do?
- Pandas gives you answers about the data. Like:
    - Is there a correlation between two or more columns?
    - What is average value?
    - Max value?
    - Min value?
- Pandas are also able to delete rows that are not relevant, or contains wrong values, like empty or NULL values. This is called cleaning the data.
## Installation of Pandas
```
pip install pandas
```
## Import Pandas
```
import pandas as pd
```
### Example:
- Program:
```
import pandas as pd
data={
	'cars':['BMW','Volvo','Ford'],
    'passing':[3,7,2]
}
dataframe=pd.DataFrame(data)
print(dataframe)
```
- Output:
```
    cars  passing
0    BMW        3
1  Volvo        7
2   Ford        2
```
### Note: alias: In Python alias are an alternate name for referring to the same thing.
## Checking the version of Pandas
- To check which version of a given Python library, say xyz , is installed, use pip show xyz or pip3 show xyz . For example, to check the version of your Pandas installation, run pip show pandas in your CMD/Powershell (Windows).
```
pip show pandas
```
## Pandas Series
- A Pandas Series is like a column in a table.
- It is a one-dimensional array holding data of any type.
### Example:
- Program:
```
import pandas as pd
a=[1,7,2]
df=pd.Series(a)
print(df)
```
- Output:
```
0    1
1    7
2    2
dtype: int64
```
### Note: It can have any type of data.
- Program:
```
import pandas as pd
a=[1, True, 'hi', 21.32,[232],{'car':'ford','year':'1992'}]
df=pd.Series(a)
print(df)
```
- Output:
```
0                                  1
1                               True
2                                 hi
3                              21.32
4                              [232]
5    {'car': 'ford', 'year': '1992'}
dtype: object
```
### Note: 0,1,2,3,4,5 are called as labels.
## Labels
- If nothing else is specified, the values are labeled with their index number. First value has index 0, second value has index 1 etc.
### Example:
- Program:
```
import pandas as pd
a=[1,8,2]
df=pd.Series(a)
print(df)
print(df[0])
```
- Output:
```
0    1
1    8
2    2
dtype: int64
1
```
## Create labels
- With the index argument, you can name your own labels.
### Example:
- Program:
```
import pandas as pd
a=[1,7,2]
df=pd.Series(a,index=['x','y','z'])
print(df)
```
- Output:
```
x    1
y    7
z    2
dtype: int64
```
- When you have created labels, you can access an item by referring to the label.
### Example:
- Program:
```
import pandas as pd
a=[1,7,2]
df=pd.Series(a,index=['x','y','z'])
print(df['z'])
```
- Output:
```
2
```
## Key/value objects in Series
- You can also use a key/value object, like a dictionary, when creating a Series.
### Example:
- Program:
```
import pandas as pd
a={'day1':420,'day2':380,'day3':390}
df=pd.Series(a)
print(df)
```
- Output:
```
day1    420
day2    380
day3    390
dtype: int64
```
### Note: The keys of the dictionary become the labels.
- To select only some of the items in the dictionary, use the index argument and specify only the items you want to include in the Series.
### Example:
- Program:
```
import pandas as pd
a={'day1':420,'day2':380,'day3':390}
df=pd.Series(a,index=['day1','day2'])
print(df)
```
- Output:
```
day1    420
day2    380
dtype: int64
```
## Pandas DataFrames
- Data sets in Pandas are usually multi-dimensional tables, called DataFrames.
- Series is like a column, a DataFrame is the whole table.
### Example:
- Program:
```
import pandas as pd
data={
	'calories':[420,380,390],
    'duration':[50,40,45]
}
df=pd.DataFrame(data)
print(df)
```
- Output:
```
   calories  duration
0       420        50
1       380        40
2       390        45
```
### Note: Compare the Series and the DataFrame.
- Program:
```
import pandas as pd
data={
	'calories':[420,380,390],
    'duration':[50,40,45]
}
df=pd.Series(data)
print(df)
```
- Output:
```
calories    [420, 380, 390]
duration       [50, 40, 45]
dtype: object
```
