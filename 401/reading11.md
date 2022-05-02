# Jyupiter and Numpy

## Jyupiter

Take so many different file formats

Jyupiter can use almost all popular image formats. As well as text formats. there is also options for terminal allowing you to integrate with your preferred rerminal.

Jyupiter notebooks oope in commnad mode which keeps Code and daa in different cells.

- [y] - Code mode
- [m] - markdown
- [a] - new line up
- [b] - new line down
- [c] - copy
- [v] - paste
- [x] - cut
- [z] - undo
- shift[z] - Redo
- [0] + [0] - Clear terminal/reset kernel

Create an equation by using $$. 

Shift+Enter in a code cell to run - all run in same terminal. 


## Numpy

Numpy is a commonly used Data Analysis tool in python. 

With Numpy you typically work in multidimension arrays. 

If you ever need to create a new arary you can do so using `numpy.zeros((3,4))` inside the parens it designates row, column so this code will create a new array with 3 rows and 4 columns.

`numpy.random.rand(3,4)` can be used in the same format as zeros but it will populate with random number data, this is good if you just need to ccheck things wih sample arrays.

`numpy.genfromtxt` is a vey handy tool that allows you to take in text files such as CSV and use them to populate tables. 

```py
games = numpy.genfromtext("gameslist.txt", delimiter="|", skip_header=1)
# Skip header will skip a number of rows
#delimiter tells it where to split the values.

```

Assigning Values to numpy arrays is also fairly simple 

`games[1,5]=donkykong` = will set second row, 6th column to calue donkeykong

You can also do this with whole rows [:,2] or whole columns [2,:] once again using row,column values. 

Numpy is interesting in that it will designate how many bits it's data types are for int and float.

`int32` is 32bit

`float64` is 64 bit

`numpy.ndarray.sum` by default finds the sum of the entire array. 

`games[1,:].sum()` 

`numpy.transpose` will filp the axis so x becomes y (row becoms column)

`numpy.ravel` Will turn an array into a one dimensional representation,

`numpy.reshape` can reshapoe an array to whatever size we want. 