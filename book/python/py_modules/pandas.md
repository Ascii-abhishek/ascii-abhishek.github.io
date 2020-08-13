# Pandas

---

```py
import pandas as pd

na_values = ['NA', 'Missing', 'Null'] # df will consider all these values as NaN
df = pd.read_csv('abc.csv', na_values=na_values)
```

## Pandas methods

| **Command**                                | **Description**                     |
| :----------------------------------------- | :---------------------------------- |
| `pd.set_option('display.max_columns', 10)` | Show 10 columns in jupyter notebook |
| `pd.set_option('display.max_rows', 40)`    | Show 40 rows in jupyter notebook    |

## Pandas property constants

| **Command**   | **Description**              |
| :------------ | :--------------------------- |
| `df.shape `   | (64, 11)                     |
| `df.columns ` | list of all columns          |
| `df.index `   | returns list of index values |
| `df.dtypes `  | data types of all pandas     |

## Pandas Methods

| **Command**                                                          | **Description**                                                                                                                   |
| :------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| `df.info() `                                                         | data_type, no_of_rows of each column                                                                                              |
| `df.head(10) `                                                       | first 10 rows, 5 if argument is not passed                                                                                        |
| `df.tail(10) `                                                       | last 10 rows, 5 if argument is not passed                                                                                         |
| `df.set_index('10_201909', inplace=False) `                          | set a column as index                                                                                                             |
| `df.sort_index(ascending=False, inplace=False) `                     | sort rows by index, descending order                                                                                              |
| `df.reset_index(inplace=True) `                                      | reset dataframe's index                                                                                                           |
| `df.rename(columns={'col1': 'val1', 'col2': 'val2'}, inplace=True) ` | rename only some column names                                                                                                     |
| `df.apply(len) `                                                     | returns length of each column, considering columns (Series) as a single entity                                                    |
| `df.applymap(len) `                                                  | len will be applied to each value of all columns (all values of df)                                                               |
| `df.drop(columns=['col1', 'col2'], index=2, inplace=False) `         | Delete multiple columns, third row                                                                                                |
| `df.drop(index=df['filter'].index) `                                 | check below for filter                                                                                                            |
| `df.append('df2', ignore_index=True, sort=False) `                   | No inplace arg here, we have to assign it to df itself                                                                            |
| `df.sort_values(by=['col_name', 'col_2'], ascending=[False, True]) ` | sort dataframe rows by col_name, first sort by col_name (descending), then by col_2 for common values in col_name (ascending)     |
| `df.nlargest(10, 'col_name') `                                       | returns df with 10 largest values of col_name                                                                                     |
| `df.nsmallest(10, 'col_name') `                                      | returns df with 10 smallest values of col_name                                                                                    |
| `df.replace('NA', numpy.nan, inplace=True) `                         | replace all NA strings in whole df with numpy nan                                                                                 |
| `df.isna() `                                                         | returns boolean df with True for NaN values                                                                                       |
| `df.fillna('other_str') `                                            | replace all NaN with other_str                                                                                                    |
| `df.to_csv('path/modified.csv') `                                    | export df to a csv file                                                                                                           |
| `df.dropna(axis='index', how='any', subset=['email'])`               | drop all rows where email is NaN, if multiple subset then drop rows where both are NaN                                            |
| -                                                                    | -                                                                                                                                 |
| `df['col_name'].sort_values() `                                      | return a sorted series                                                                                                            |
| `df['col_name'].nlargest(10) `                                       | highest 10 values of col_name, returns series                                                                                     |
| `df['10_201909'].value_counts() `                                    | count frequency of all unique values in 10_201909 column                                                                          |
| `df['age'].astype(float) `                                           | by default numbers are parsed as strings, and we can convert np.NaN to float but not int so best practice to convert all to float |
| `df['age'].mean() `                                                  | returns mean of age column                                                                                                        |
| `df['age'].unique() `                                                | returns a list of all unique values in the age column                                                                             |
| `df['age'].replace('text', 0, inplace=True) `                        | replace text with 0                                                                                                               |

## Accessing 

### columns

| **Command**                                    | **Description**            |
| :--------------------------------------------- | :------------------------- |
| `df['10_201909'] `                             | accessing '10_201909'      |
| `df[['10_201909', '10_201910', '10_201909']] ` | accessing multiple columns |

### rows

| **Command**                                                  | **Description**                                     |
| :----------------------------------------------------------- | :-------------------------------------------------- |
| `df.iloc[1]`                                                 | accesing second (single) row, index starting from 0 |
| `df.iloc[[0, 1, 3, 7]]`                                      | accessing multiple rows                             |
| `df.iloc[[2, 5], 1]`                                         | second column, third and sixth rows                 |
| `df.iloc[[1, 5], [3, 8]]`                                    | accessing via multiple rows and column (indexes)    |
| ---                                                          | ---                                                 |
| `df.loc[[0, 1, 3], ['10_201909', '10_201910', '10_201909']]` | accessing via labels instead of indexes             |
| `df.loc[0:21, '10_201909']`                                  | 0 to 21 (inclusive row values of 10_201909 column)  |
| `df.loc[0:5, '10_201909': '10_201912']`                      | row and column slicing                              |

