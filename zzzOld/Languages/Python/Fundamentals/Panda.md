- Pandas is a Python library.
- Pandas is used to analyze data.

## What is Pandas?
- Pandas is a Python library used for working with data sets.
- It has functions for analyzing, cleaning, exploring, and manipulating data.
- The name "Pandas" has a reference to both "Panel Data", and "Python Data Analysis" and was created by Wes McKinney in 2008.

## Why Use Pandas?
- Pandas allows us to analyze big data and make conclusions based on statistical theories.
- Pandas can clean messy data sets, and make them readable and relevant.
- Relevant data is very important in data science.

## What Can Pandas Do?

Pandas gives you answers about the data. Like:
-   Is there a correlation between two or more columns?
-   What is average value?
-   Max value?
-   Min value?

Pandas are also able to delete rows that are not relevant, or contains wrong values, like empty or NULL values. This is called _cleaning_ the data.

## Installing Pandas

*In the terminal:*
```
pip install pandas
```

##  Printing a normal List vs Pandas 

*Printing using a **normal list***
```python
column = ["Meow meow", "Whitey", "Spot"]
print(column)
#Output: ['Meow meow', 'Whitey', 'Spot']
```

*Printing using **Pandas***
```python
import pandas as pd

column = ["Meow meow", "Whitey", "Spot"]
data = pd.DataFrame(column)
print(data)

#OUTPUT:
#            0
# 0  Meow meow
# 1     Whitey
# 2       Spot
```

The Pandas library is built on NumPy and provides easy-to-use **data structures** and **data analysis** tools for the Python programming language.

## pd.Series()

A **one dimensional** labeled array capable of holding any data type.
```python
import pandas as pd
data = pd.Series(["Meow meow", "Whitey", "Spot"])
print(data)
```
```output
# OUTPUT:
0    Meow meow
1       Whitey
2         Spot
```

If nothing else is specified, the values are labeled with their index number. First value has index 0, second value has index 1 etc.

With the `index` argument, you can name your own labels:

```python
import pandas as pd

data = pd.Series(["Meow meow", "Whitey", "Spot"], index=["Cat 1", "Cat 2", "Cat 3"])
print(data)
```
```output
#OUTPUT:
# Cat 1    Meow meow
# Cat 2       Whitey
# Cat 3         Spot
```

## pd.DataFrame()

A **two dimensional** labeled data structure with columns of potentially different types.

```python
import pandas as pd

column = ["Meow meow", "Whitey", "Spot"]
data = pd.DataFrame({"Names:": column,
                     "Weight:": [8, 4.33, 3],
                     "Height:": [3, 2.9, 2.6]})
print(data)
```
```output
#OUTPUT:
#       Names:  Weight:  Height:
# 0  Meow meow     8.00      3.0
# 1     Whitey     4.33      2.9
# 2       Spot     3.00      2.6
```

## Selecting Data

```python
import pandas as pd

column = ["Meow meow", "Whitey", "Spot"]
data = pd.DataFrame({"Names:": column,
                     "Weight:": [8, 4.33, 3],
                     "Height:": [3, 2.9, 2.6]})
print(data)

#OUTPUT:
#       Names:  Weight:  Height:
# 0  Meow meow     8.00      3.0
# 1     Whitey     4.33      2.9
# 2       Spot     3.00      2.6
```

### To select a specific row or column
```python
sel_col = data["Names:"]
print(sel_col)

#OUTPUT:
# 0    Meow meow
# 1       Whitey
# 2         Spot
```

```python
sel_row = data.iloc[1]
print(sel_row)

#OUTPUT:
# Names:     Whitey
# Weight:      4.33
# Height:       2.9
# Name: 1, dtype: object
```

### To Select a Specific Data
```python
sel_col = data["Weight:"][1]  
sel_row = data.iloc[1]["Weight:"]
print(sel_row)
print(sel_col)

#OUTPUT:
# 4.33
# 4.33
```

## Manipulating Data
```python
import pandas as pd

column = ["Meow meow", "Whitey", "Spot"]
data = pd.DataFrame({"Names:": column,
                     "Weight:": [8, 4.33, 3],
                     "Height:": [3, 2.9, 2.6]})

# Computes the bmi list by selecting the height and weight cols
bmi = []
for i in range(len(data)):
    height = data["Height:"][i]
    weight = data["Weight:"][i]
    bmi_score = weight / (height**2)
    bmi.append(bmi_score)
    
# adds the bmi list into data which is a dict
data["BMI:"] = bmi

print(data)

#OUTPUT:
#       Names:  Weight:  Height:      BMI:
# 0  Meow meow     8.00      3.0  0.888889
# 1     Whitey     4.33      2.9  0.514863
# 2       Spot     3.00      2.6  0.443787
```

## Saving Data

```python
data.to_csv("bmi.txt")
data.to_csv("bmi.csv")

#OUTPUT:
# ,Names:,Weight:,Height:,BMI:
# 0,Meow meow,8.0,3.0,0.8888888888888888
# 1,Whitey,4.33,2.9,0.5148632580261593
# 2,Spot,3.0,2.6,0.44378698224852065
```

```python
data.to_csv("bmi.txt", sep="\t")
data.to_csv("bmi.csv", sep="\t")

#OUTPUT:
#   Names:  Weight: Height: BMI:
# 0 Meow meow   8.0 3.0 0.8888888888888888
# 1 Whitey  4.33    2.9 0.5148632580261593
# 2 Spot    3.0 2.6 0.44378698224852065
```

**NOTE:** sep means seperator, the defaul is the commas from the first output. Seperators can only be 1 character / 1 letter long.

## Reading Save Files

```python
import pandas as pd

data = pd.read_csv("bmi.txt", sep="\t")
print(data)
  
#OUTPUT
#    Unnamed: 0     Names:  Weight:  Height:      BMI:
# 0           0  Meow meow     8.00      3.0  0.888889
# 1           1     Whitey     4.33      2.9  0.514863
# 2           2       Spot     3.00      2.6  0.443787
```

**NOTE:** To note have doubled index then don't save the index in the first place.

```python
data.to_csv("bmi.txt", sep="\t", index=False)
```


## Display

If you have a large DataFrame with many rows, Pandas will only return the first 5 rows, and the last 5 rows

To display the **entire** data (even thousands of data)
```python
print(data.to_string())
```

To increase the maximum number of rows to display the entire DataFrame
```python
pd.options.display.max_rows = 9999
```

## Check Pandas Version

The version string is stored under `__version__` attribute.
```python
import pandas as pd  
print(pd.__version__)
```

```output
2.0.1
```

## Locating Rows (loc)

Pandas use the `loc` attribute to return one or more specified row(s)

```python
import pandas as pd
data = pd.DataFrame({"Names:": ["Meow meow", "Whitey", "Spot"],
                     "Weight:": [8, 4.33, 3],
                     "Height:": [3, 2.9, 2.6]})
print(data.loc[1])
```
```output
# OUTPUT:
      Names:  Weight:  Height:
0  Meow meow     8.00      3.0
1     Whitey     4.33      2.9
2       Spot     3.00      2.6
```

using the example above:
```python
print(df.loc[0])
```
```output
# OUTPUT:
Names:     Whitey
Weight:      4.33
Height:       2.9
Name: 1, dtype: object
```

# loc vs iloc
- `iloc[]` uses integer only for indexing
- `iloc[]` can do slicing using integer (the range is NOT included)
- `loc[]` can us integer and also keywords for indexing
- `loc[]` can do slicing using strings (the range IS included)

Both `loc[]` and `iloc[]` uses the syntax `loc[row, column]`.

```python
import pandas as pd
data = pd.DataFrame({"Names:": ["Meow meow", "Whitey", "Spot"],
                     "Weight:": [8, 4.33, 3],
                     "Height:": [3, 2.9, 2.6]},
                     index = ["cat1", "cat2", "cat3"])
print(data)
```
```output
# OUTPUT:
         Names:  Weight:  Height:
cat1  Meow meow     8.00      3.0
cat2     Whitey     4.33      2.9
cat3       Spot     3.00      2.6
```


### `iloc` with an int index
```python
print(data.iloc[0])
```
```output
# OUTPUT:
Names:     Meow meow
Weight:          8.0
Height:          3.0
Name: cat1, dtype: object
```

### `iloc` with a str index
```python
print(data.iloc["cat1"])
```
```output
# OUTPUT:
TypeError: Cannot index by location index with a non-integer key
```

### `iloc` with slicing
```python
print(data.iloc[0:2])
```
```output
# OUTPUT:
         Names:  Weight:  Height:
cat1  Meow meow     8.00      3.0
cat2     Whitey     4.33      2.9
```

### `loc` with an int index
```python
print(data.loc[0])
```
```output
# OUTPUT:
raise KeyError(key) from err
KeyError: 0
```
***Note:** this raise an error because the example's index is already a string however if it is still an int, this will run.*

### `loc` with a str index
```python
print(data.loc["cat1"])
```
```output
# OUTPUT
Names:     Meow meow
Weight:          8.0
Height:          3.0
Name: cat1, dtype: object
```

### `loc` with slicing
```python
print(data.loc["cat1":"cat3"])
```
```output
# OUTPUT:
         Names:  Weight:  Height:
cat1  Meow meow     8.00      3.0
cat2     Whitey     4.33      2.9
cat3       Spot     3.00      2.6
```

## Large DataFrame
- If you have a large DataFrame with many rows, Pandas will only return the first 5 rows, and the last 5 rows
- use `to_string()` to print the entire DataFrame.
- The number of rows returned is defined in Pandas option settings.
- You can check your system's maximum rows with the `pd.options.display.max_rows` statement.

```python
import pandas as pd  
print(pd.options.display.max_rows)
```
```output
# OUTPUT:
60
```

## Data Analysis

### Head( )
- One of the most used method for getting a quick overview of the DataFrame, is the `head()` method.

The `head()` method returns the headers and a specified number of rows, starting from the top.
```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.head(10))
```
```output
# OUTPUT:
   Duration  Pulse  Maxpulse  Calories
0        60    110       130     409.1
1        60    117       145     479.0
2        60    103       135     340.0
3        45    109       175     282.4
4        45    117       148     406.0
5        60    102       127     300.5
6        60    110       136     374.0
7        45    104       134     253.3
8        30    109       133     195.1
9        60     98       124     269.0
```

if you don't specify how many rows you would like to return, will on return 5 rows.
```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.head())
```
```output
# OUTPUT:
   Duration  Pulse  Maxpulse  Calories
0        60    110       130     409.1
1        60    117       145     479.0
2        60    103       135     340.0
3        45    109       175     282.4
4        45    117       148     406.0
```

### Tail( )
- There is also a `tail()` method for viewing the _last_ rows of the DataFrame.

The `tail()` method returns the headers and a specified number of rows, starting from the bottom.
```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.tail())
```
```output
# OUTPUT:
     Duration  Pulse  Maxpulse  Calories
164        60    105       140     290.8
165        60    110       145     300.4
166        60    115       145     310.2
167        75    120       150     320.4
168        75    125       150     330.4
```

### info( )
The DataFrames object has a method called `info()`, that gives you more information about the data set.

```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.info())
```
```output
# OUTPUT:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 169 entries, 0 to 168
Data columns (total 4 columns):
 #   Column    Non-Null Count  Dtype  
---  ------    --------------  -----  
 0   Duration  169 non-null    int64  
 1   Pulse     169 non-null    int64  
 2   Maxpulse  169 non-null    int64  
 3   Calories  164 non-null    float64
dtypes: float64(1), int64(3)
memory usage: 5.4 KB
None
```

#### ANALYSIS:
```
RangeIndex: 169 entries, 0 to 168
Data columns (total 4 columns):
```
The result tells us there are 169 rows and 4 columns

```
   #   Column    Non-Null Count  Dtype  
  ---  ------    --------------  -----  
   0   Duration  169 non-null    int64  
   1   Pulse     169 non-null    int64  
   2   Maxpulse  169 non-null    int64  
   3   Calories  164 non-null    float64
```
It seems like there are 164 of 169 Non-Null values in the "Calories" column.

## Removing Empty Rows
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
new_df = df.dropna()  
print(new_df.to_string())
```
***Note:** This will create a new df that is different from the original df*

Use the argument `inplace = True` to also change the original df
```python
new_df = df.dropna(inplace = True) 
```

### To Replace only Specified Columns
```python
df.dropna(subset=['Date'], inplace = True)
```

## Filling Empty Rows
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
df.fillna(130, inplace = True)
```

### To Replace only Specified Columns
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
df["Calories"].fillna(130, inplace = True)
```

## Mean, Median, Mode of a Column

### Mean
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
mean = df["Calories"].mean()
print(mean)
```

## Median
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
median = df["Calories"].median()
print(median)
```

## Mode
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
mode = df["Calories"].mode()[0]
print(mode)
```
***Note:** the* `mode()` *returns a list so get the first element* `[0]`

## Correcting the Format

### Date
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
df['Date'] = pd.to_datetime(df['Date'])  
print(df.to_string())
```
This will correct the  date data if it is **correctable**.
If it is not, like the data is empty, you should just remove it.

```python
df.dropna(subset=['Date'], inplace = True)
```

## Fixing Wrong Data
- "Wrong data" does not have to be "empty cells" or "wrong format", it can just be wrong, like if someone registered "199" instead of "1.99".
- Basically it's a typo.

### Removing non-empty rows
```python
import pandas as pd  
df = pd.read_csv('data.csv')  
new_df = df.drop(2)  
print(new_df.to_string())
```

## Removing Duplicate
```
    Duration          Date  Pulse  Maxpulse  Calories
0         60  '2020/12/01'    110       130     409.1
1         60  '2020/12/02'    117       145     479.0
2         60  '2020/12/03'    103       135     340.0
3         45  '2020/12/04'    109       175     282.4
4         45  '2020/12/05'    117       148     406.0
5         60  '2020/12/06'    102       127     300.0
6         60  '2020/12/07'    110       136     374.0
7        450  '2020/12/08'    104       134     253.3
8         30  '2020/12/09'    109       133     195.1
9         60  '2020/12/10'     98       124     269.0
10        60  '2020/12/11'    103       147     329.3
11        60  '2020/12/12'    100       120     250.7
12        60  '2020/12/12'    100       120     250.7
13        60  '2020/12/13'    106       128     345.3
```

To discover duplicates, we can use the `duplicated()` method.
```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.duplicated())
```
```output
# OUTPUT:
0     False
1     False
2     False
3     False
4     False
5     False
6     False
7     False
8     False
9     False
10    False
11    False
12     True
13    False
```
line 12 is a duplicate of line 11

To remove duplicates, use the `drop_duplicates()` method.
```python
df.drop_duplicates(inplace = True)
```



