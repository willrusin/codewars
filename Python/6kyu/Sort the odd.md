# CodeWars Python Solutions

---

## Sort the odd


**Definition**

You will be given an array of numbers. You have to sort the odd numbers in ascending order while leaving the even numbers at their original positions.

Examples
[7, 1]  =>  [1, 7]
[5, 8, 6, 3, 4]  =>  [3, 8, 6, 5, 4]
[9, 8, 7, 6, 5, 4, 3, 2, 1, 0]  =>  [1, 8, 3, 6, 5, 4, 7, 2, 9, 0]

### Sample Tests]
```Python
test.assert_equals(sort_array([5, 3, 2, 8, 1, 4]), [1, 3, 2, 8, 5, 4])
test.assert_equals(sort_array([5, 3, 1, 8, 0]), [1, 3, 5, 8, 0])
test.assert_equals(sort_array([]),[])
```
---

### Given Code


```python
def sort_array(source_array):
    # Return a sorted array.

```

---

### my initital Solution


```python
def sort_array(source_array):
    working = sorted([i for i in source_array if i %2 != 0]) #create a sorted array of the odd numbers
    odd_int = 0
    for i in range(len(source_array)):
        if source_array[i] %2 != 0: #if odd
            source_array[i] = working[odd_int] #replace with next sorted value
            odd_int += 1 #increment
    return source_array
    
```

---


[See on CodeWars.com](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/train/python)