# Numpy

## install


```python
# terminal commands ausfuehren mit `!`

!mkdir test
```

    mkdir: test: File exists



```python
# python module installieren fuer die 'richtige' python-version,
# die auch im Notebook verwendet wird

import sys

!{sys.executable} -m pip install numpy

# equivalent to:
# /Users/<username>/miniconda3/bin/python -m pip install numpy
# or similar
```

    Requirement already satisfied: numpy in /Users/danielhopfner/miniconda3/lib/python3.9/site-packages (1.21.5)


## Import


```python
import numpy as np
```

## Numpy-Arrays vs. Listen


```python
a = np.array([1, 2, 3, 4])
```


```python
print(a)
```

    [1 2 3 4]



```python
l = [1, 2, 3, 4]
```


```python
l
```




    [1, 2, 3, 4]



### elementweise Operationen


```python
a_1 = np.array([1,   2,   3,   4])
a_2 = np.array([200, 300, 400, 500])

a_1 + a_2
```




    array([201, 302, 403, 504])




```python
l_1 = [1, 2, 3, 4]
l_2 = [200, 300, 400, 500]

l_1 + l_2 # listen muessten elementweise verrechnet werden durch loops
```




    [1, 2, 3, 4, 200, 300, 400, 500]




```python
# array concatenation
np.concatenate([a_1, a_2])
```




    array([  1,   2,   3,   4, 200, 300, 400, 500])




```python
# --------------------------------------------------------
# Jupyter shortcuts for auto-completion and documentation:

# np.conc # -> Tab --> auto-completion

# np.concatenate() # mit cursor innerhalb der klammern:
# Shift-Tab 
```


```python
# elementweise Operationen funktionieren mit (fast) allen moeglichen Funktionen

print(a_1 + a_2, '\n')

print(a_1 - a_2, '\n')

print(a_1 * a_2, '\n')

print(a_2 ** a_1, '\n')

print(np.array([2, 5, 8, 13]) > np.array([3, 4, 10, 12]), '\n')
```

    [201 302 403 504] 
    
    [-199 -298 -397 -496] 
    
    [ 200  600 1200 2000] 
    
    [        200       90000    64000000 62500000000] 
    
    [False  True False  True] 
    


### Datentypen


```python
l = [1, 2.0, 'hallo']
pril_1 = [1, 2, 3, 4]
# l_2 = [200, 300, 400, 500]nt(l)
print(type(l[0]))
print(type(l[1]))
print(type(l[2]))
```

    <class 'int'>
    <class 'float'>
    <class 'str'>



```python
a = np.array([1, 2.0, 'hallo'])
print(a)
print(type(a[0]))
print(type(a[1]))
print(type(a[2]))
```

    ['1' '2.0' 'hallo']
    <class 'numpy.str_'>
    <class 'numpy.str_'>
    <class 'numpy.str_'>


### Recheneffizienz

**`zip`**:


```python
for element in [1, 2, 3, 4]:
    print(element)



l_1 = [1, 2, 3, 4]
l_2 = [200, 300, 400, 500]

print()

for i in range(len(l_1)):
    print( l_1[i] + l_2[i] )
    

print()
    
# zip


for el_1, el_2 in zip(l_1, l_2):
    
    print(el_1, el_2)

```

    1
    2
    3
    4
    
    201
    302
    403
    504
    
    1 200
    2 300
    3 400
    4 500



```python
# listen elementweise verrechnen

def add_element_wise(l_1, l_2):
    
    added_list = []
    
    for el_1, el_2 in zip(l_1, l_2):
        
        added_list.append(el_1 + el_2)
        
    return added_list

add_element_wise(l_1, l_2)
```




    [201, 302, 403, 504]




```python
l_1 = []
l_2 = []

for i in range(10000000):
    
    l_1.append(i)
    l_2.append((i + 2) * 100)
    
add_element_wise(l_1, l_2)
```




    [200,
     301,
     ...
     100998,
     101099,
     ...]




```python
a_1 = np.array(l_1)
a_2 = np.array(l_2)
```


```python
a_1 + a_2
```




    array([       200,        301,        402, ..., 1009999897, 1009999998,
           1010000099])




```python
%timeit add_element_wise(l_1, l_2)
```

    579 ms ± 2.79 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)



```python
%timeit a_1 + a_2
```

    7.9 ms ± 377 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)

