NumPy stands for Numerical Python. It a python library used for numerical computation widely used in field requiring heavy data processing such as data science, data engineering, AI/ML. Python being easy to ready/write, having many libraries, easy to integrate APIs, databases, web apps etc. Python is heavily preferred in such fields.

But python is a really slow language. NumPy under the hood is written in C which is much faster.


## Installation and Use

directly through terminal : `pip install numpy`
through jupyter block : `!pip install numpy` 
through jupyter block safer: `%pip install numpy`
then, 
`Import numpy as np`

## Why NumPy over list ?

Python has lists but its very slow and for more complex computation like matrix multiplication, inverse matrices etc. it wont work. So NumPy has built in `np.array([])` which is much function it also has built in functions which can find eigenvalues and eigenvectors, inverse matrices, transpose matrices etc.
```
# in python list if we want to multiply all items with certain number i.e, scalar multiplication
my_list = [1,2,3,4,5]
print(my_list * 2)
output : [1,2,3,4,5,1,2,3,4,5]
# It just duplicates it, we can solve it by running loop but it would be tideous. 

#Numpy has prebuilt feature to do it 
my_list = np.array([1,2,3,4,5])
print(my_list * 2)
output : [2,4,6,8,10]
```

>[! Note]
>Normal python list is of type list so for first if we do `print(type(my_list))` --> `<class 'list'>`
>But numpy array is a different type it is n-dimensional array. So for second `print(type(my_list))` --> `<class 'numpy.ndarray'>`

## Commands

- `print(np.__version__)` : prints the NumPy version
- `np.array([])` : turns python list to NumPy array.

### N - Dimensional array

- `np.array(arr.ndim)` : used to check the number of dimension of arr. For ex :
	- `np.array("Abc").ndim` : 0
	- `np.array([1,2,3,4]).ndim` : 1
	- `np.array([[1,2,3],[3,4,5]]).ndim` : 2, which we can refer as 2*3 matrix in 2D.
	-  `np.array([[1,2,3],[3,4]]).ndim`: error NumPy expects a homogenous matrix.
	- `np.array([[[],[],[]],[[],[],[]]]).ndim`: 3, for 3D. 
- `np.array(arr.shape)` : shows the shape of arr in tuple format of (rows, cols). For ex :
	- `np.array("Abc").shape` : ()
	- `np.array([1,2,3,4]).shape` :  (4,)
	- `np.array([[1,2,3],[3,4,5]]).shape` : (2, 3)
	- `np.array([[1,2,3],[3,4]]).shape` :  error.

### Accessing items

Unlike in normal python list where we use `array[0][0]`(can still use this format in NumPy). In NumPy, we can simply access in one bracket with comma separation
- `array[0,1]` : get item of 0 row and 1 col.

## Slicing array

### Row slicing

***`array[start : stop : step]` end is exclusive***
```
arr = np.array([[1, 2, 3, 4],
                [5, 6, 7, 8],
                [9, 10, 11, 12],
                [13, 14, 15, 16]])
```
- `array[0]` it gives the array at first index : `[1,2,3,4]`.
- `array[0:]` if nothing is given start from 0 go till end, so this basically return the entire array back.
- `array[0,3]` return the first and second array : `[[1,2,3,4],[5,6,7,8]]`.
- `array[0::2]` start from first go till end but jump two index : `[[1,2,3,4],[9,10,11,12]]`.
- `array[::-1]` basically reverse the array.

### Column slicing

***`array[row,col]`*** this is for 2D . Row must have some value or else it give error. 
- `array[:, 0]` select all rows from first to last and select column 0 : `[1,5,9,13]`
- `array[1:3, 1:3]` select rows 1 and 2 , cols 1 and 2 : `[[6,7],[10,11]]`