# Pandas DataFrames
## DataFrame 
- A Pandas DataFrame is a 2 dimensional data structure, like a 2 dimensional array, or a table with rows and columns.
### Example:
- Program:
```
import pandas as pd
a={'calories':[420,380,390],
   'duration':[50,40,45]
   }
df=pd.DataFrame(a)
print(df)
```
- Output:
```
   calories  duration
0       420        50
1       380        40
2       390        45
```
### Locate row
- As you can see from the result above, the DataFrame is like a table with rows and columns.
- Pandas use the ```loc``` attribute to return one or more specified row(s)
#### Example:
- Program:
```
import pandas as pd
a={'calories':[420,380,390],
	'duration':[50,40,45]}
df=pd.DataFrame(a)
print(df.loc[0])
```
- Output:
```
calories    420
duration     50
Name: 0, dtype: int64
```
- Program:
```
import pandas as pd
a={'calories':[420,380,390],
	'duration':[50,40,45]}
df=pd.DataFrame(a,index=['a','b','c'])
print(df.loc['b'])
```
- Output:
```
calories    380
duration     40
Name: b, dtype: int64
```
### Note: The above example returns a Pandas Series.
- Program:
```
import pandas as pd
a={'calories':[420,380,390],
'duration':[50,40,45]}
df=pd.DataFrame(a)
print(df)
print('')
print(df.loc[[0,1]]) #use a list of indexes
```
- Output:
```
   calories  duration
0       420        50
1       380        40
2       390        45

   calories  duration
0       420        50
1       380        40
```
### Note: When using ```[]```, the result is a Pandas DataFrame.
## Named Indexes:
- With the index argument, you can name your own indexes.
### Example:
- Program:
```
import pandas as pd
a={'calories':[420,380,390],
	'duration':[50,40,45]}
df=pd.DataFrame(a,index=['day1','day2','day3'])
print(df)
```
- Output:
```
      calories  duration
day1       420        50
day2       380        40
day3       390        45
```
### Locate named indexes:
- ```loc``` is used to locate named indexes.
#### Example:
- Program:
```
import pandas as pd
a={'calories':[420,380,390],
'duration':[50,40,45]}
df=pd.DataFrame(a,index=['day1','day2','day3'])
print(df)
print('')
print(df.loc['day1'])
print('')
print(df.loc[['day1','day2']]) # use index as lists
```
- Output:
```
      calories  duration
day1       420        50
day2       380        40
day3       390        45

calories    420
duration     50
Name: day1, dtype: int64

      calories  duration
day1       420        50
day2       380        40
```
### Load files into a DataFrame
- If your data sets are stored in a file, Pandas can load them into a DataFrame.
#### Example:
- Program:
```
import pandas as pd
df=pd.read_csv('data.csv')
print(df)
```
- Output:
```
     Duration  Pulse  Maxpulse  Calories
0          60    110       130     409.1
1          60    117       145     479.0
2          60    103       135     340.0
3          45    109       175     282.4
4          45    117       148     406.0
..        ...    ...       ...       ...
164        60    105       140     290.8
165        60    110       145     300.4
166        60    115       145     310.2
167        75    120       150     320.4
168        75    125       150     330.4

[169 rows x 4 columns]
```
### Note: 'data.csv' is present in the repository.
