# QuickDataFrame
A quick simple table data structure in Python which is basicaly a `dict` of `list`s.

The simple table would be like this:

| row number | col1           | col2           | col3           |
| :--------: | :------------: | :------------: | :------------: |
| **0**      | qdf['col1'][0] | qdf['col2'][0] | qdf['col3'][0] |
| **1**      | qdf['col1'][1] | qdf['col2'][1] | qdf['col3'][1] |
| **2**      | qdf['col1'][2] | qdf['col2'][2] | qdf['col3'][2] |

In which each column is a Python `list` that are all stored in a Python `dict`.

## How to use
To create a QDF simply give it a list of column names, or don't (you can add column later)

```python
qdf = QuickDataFrame(['name', 'school', 'id'])
```


Then to add rows you have the following options
```python
# append a row and fill it with a  specific value
qdf.append(value='def')
# append a row using a list
qdf.append(row=['Amir', 'AUT', 56])
# append a row using a dict
qdf.append(row={'name':'Amir', 'school':'AUT', 'id':56})
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
```
There are also `to_csv` and `read_csv` methods.


I'll explain other features later.