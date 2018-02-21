# QuickDataFrame
A quick simple table data structure in Python which is basicaly a `dict` of `list`s.
The simple table would be like this:
| row number | col1           | col2           | col3           |
| :--------: | :------------: | :------------: | :------------: |
| **0**      | qdf['col1'][0] | qdf['col2'][0] | qdf['col3'][0] |
| **1**      | qdf['col1'][1] | qdf['col2'][1] | qdf['col3'][1] |
| **2**      | qdf['col1'][2] | qdf['col2'][2] | qdf['col3'][2] |

In which each column is a Python `list` that are all stored in a Python `dict`.
