# QuickDataFrame
A quick simple table data structure in Python which is basicaly a `dict` of `list`s.

The simple table would be like this:

|     | column1 | column2 | column3 |
:---: | :-----: | :-----: | :-----: |
_0_   | 45  | [3,4,6] | 'pavement'  |
_1_   |  0.234  | 0       |  None   |
_2_   | {'as','re'} | (5,0)  |  's' |
_3_   | 4 | 1  |  9 |

In which each column is a Python `list` that are all stored in a Python `dict`.

## How to use
To create a QDF simply give it a list of column names, or don't (you can add columns later)
```python
qdf = QuickDataFrame(['name', 'school', 'id'])
# or add columns later
qdf = QuickDataFrame()
qdf.add_column('name')
```


Then to add rows you have the following options
```python
# append a row using a list
qdf.append(row=['Amir', 'AUT', 56])
# append a row using a dict
qdf.append(row={'name':'Amir', 'school':'AUT', 'id':56})
# append a row and fill it with a specific value
qdf.append(value='def')
# append a row and fill it with None
qdf.append()
```
You could set a value in previously appended rows as well
```python
qdf['id'][1] = 91
```
Now to access the data
```python
# to get a cell in the table
print(qdf['name'][1])
# to get a row
print(qdf[1])
# to get a column
print(qdf['name'])
# to get a slice of rows as a new QDF
print(qdf[3:14])
# to get a list of columns as a new QDF
print(qdf[['name', 'id']]) 
```
There are also `to_csv` and `read_csv` methods.


I'll explain the other features later.