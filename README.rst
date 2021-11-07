**Snutshell** is a Python module for storing numeric data in dat and xlsx format

All the functionalities are explained using simple examples:


**create_xlsx** function
.. code-block:: python
        
..from snutshell import create_xlsx
..list1 = [2, 3, 5, 7, 11]
..list2 = [1, 3, 5, 7, 9, 11, 13, 15]
..# we want to save the two lists into a xlsx file
..# For this, we have to create a dictionary 
..dict = {'primes' : list1, 'odds': list2}  # dictionary keys will be used as data title
..create_xlsx('filename.xlsx', dict)
.. image:: https://github.com/naziulhaque/Snutshell/blob/master/docs/s1.PNG


.. code-block:: python
..# you can also save 2d numpy arrays or nested list     
..from snutshell import create_xlsx
..import numpy as np
   list1 = [['a', 'b', 'c'], ['apple', 'banana', 'cat']]
   list2 = np.array([[5,6], [7,8]]) 
   dict = {'title1' : list1, 'title2': list2} 
   create_xlsx('filename.xlsx', dict)

   #instead of supplying a dictionary, we can also provide two lists: one containing the keys, 
   and the other containing the values. The following line is equivalent to the previous line.
   create_xlsx('filename.xlsx', ['title1', 'title2'], [list1, list2])

.. image:: https://github.com/naziulhaque/Snutshell/blob/master/docs/s2.PNG

.. code-block:: python
   # you can also save some weird data 
   dict = {'habijabi': 'alum-halum khalum', 'time':300, 'a weird dictionary': {1:[1,2,3],2:3,3:5,4:7}, 42:[['aanjk', 'ajvnk', 'gnkja'],[1,2,3]]}   
   create_xlsx('filename.xlsx', dict)    # observe the way a dictionary input is saved
.. image:: https://github.com/naziulhaque/Snutshell/blob/master/docs/s3.PNG


