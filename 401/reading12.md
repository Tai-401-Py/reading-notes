# [10 minutes to Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

## Object Creation

`pd.Series([value,value, ...])` - By passing a list of values, pandas will create a default integer index.


You can also create a DataFrame

`pd.date_range("20130101", periods=6)`  Creates a data frame witha  datetime index... 

you can also create a dataframe creatinga  series like sturcture

```py
 df2 = pd.DataFrame(
    {
        "A": 1.0,
        "B": pd.Timestamp("20130102"),
        "C": pd.Series(1, index=list(range(4)), dtype="float32"),
        "D": np.array([3] * 4, dtype="int32"),
        "E": pd.Categorical(["test", "train", "test", "train"]),
        "F": "foo",
    }
Out[10]: 
     A          B    C  D      E    F
0  1.0 2013-01-02  1.0  3   test  foo
1  1.0 2013-01-02  1.0  3  train  foo
2  1.0 2013-01-02  1.0  3   test  foo
3  1.0 2013-01-02  1.0  3  train  foo
```

### Viewing Data

`df.head()` will allow you to view the whole data table

`df.tail(#)` will allow you to see the last # of entries

`df.index()` Will show you the indexes of the table

`df.columns()` Will show you the columns of the table. 
`df.describe()` shows quick stats 

 While standard Python / NumPy expressions for selecting and setting are intuitive and come in handy for interactive work, for production code, we recommend the optimized pandas data access methods, .at, .iat, .loc and .iloc.

`df["A"]` - returns column with title A

`df[0:3]` - returns index colummns between 0 and 3

`df["20130102":"20130104"]` - will return rows between those datetimes

`df.iloc[]` - selction by position of passed integers

You can also do by slices `[row, col]` - `[3:5, 0:2]` from 3 to 5 and 0 to 2

`df.isin()` will search

Settinga  new column will automatically align data by indexes.


If you're missing data it will return NaN

Operations will skip missing values

Series is equipped with string methods like `.lower` to affect string data