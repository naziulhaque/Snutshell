# Snutshell


**Snutshell** is a Python library for storing numeric data in dat and xlsx format

All the functionalities are explained using simple examples.
### 1. *create_xlsx* function

```python        
    from snutshell import create_xlsx
    list1 = [2, 3, 5, 7, 11]
    list2 = [1, 3, 5, 7, 9, 11, 13, 15]
    # we want to save the two lists into a xlsx file
    # For this, we have to create a dictionary 
    dict = {'primes' : list1, 'odds': list2}  # dictionary keys will be used as data title
    create_xlsx('filename.xlsx', dict)
```
![image1](https://github.com/naziulhaque/Snutshell/blob/master/docs/s1.PNG)
:--:| 
**Figure 1** |





### 2. You can also save 2D numpy arrays or nested list.   

```python
    from snutshell import create_xlsx
    import numpy as np
    list1 = [['a', 'b', 'c'], ['apple', 'banana', 'cat']]
    list2 = np.array([[5, 6], [7, 8]]) 
    dict = {'title1' : list1, 'title2': list2} 
    create_xlsx('filename.xlsx', dict)
```

#### Instead of supplying a dictionary, we can also provide two lists: one containing the keys, and the other containing the values. The following line is equivalent to the last line of the previous code block.

```python
   create_xlsx('filename.xlsx', ['title1', 'title2'], [list1, list2])
```
![image2](https://github.com/naziulhaque/Snutshell/blob/master/docs/s2.PNG)
:--:| 
**Figure 2** |


### 3. You can also save some weird data.

```python
   dict = {'habijabi': 'alum-halum khalum', 'time': 300, 'a weird dictionary': {1 : [1,2,3], 2 : 3, 3 : 5, 4 : 7}, 42 : [['aanjk', 'ajvnk', 'gnkja'],[1, 2, 3]]}   
   create_xlsx('filename.xlsx', dict)    # observe the way a dictionary input is saved
```   
![image3](https://github.com/naziulhaque/Snutshell/blob/master/docs/s3.PNG)
:--:| 
**Figure 3** |

### 4. You can save the file in DAT format also. DAT file saves the data as python dictionary. For this you have to use a keyword argument which is illustrated using the following example.

```python
    dict = {'habijabi': 'alum-halum khalum', 'time':300, 'a weird dictionary': {1:[1,2,3],2:3,3:5,4:7}, 42:[['aanjk', 'ajvnk', 'gnkja'],[1,2,3]]}   
    create_xlsx('filename.xlsx', dict, dat = True)
```

### 5. *load* function

This function loads a DAT file (which was created from a python dictionary in the first place) as python dictionary.

```python
    from snutshell import load
    dict = load('filename.dat')
``` 
