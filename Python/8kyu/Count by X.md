# CodeWars Python Solutions

---

## Count by X


**Definition**

Create a function with two arguments that will return an array of the first n multiples of x.

Assume both the given number and the number of times to count will be positive numbers greater than 0.

Return the results as an array or list ( depending on language ).

Examples
count_by(1,10) #should return [1,2,3,4,5,6,7,8,9,10]
count_by(2,5) #should return [2,4,6,8,10]


### Sample Tests]
```Python
import codewars_test as test
from solution import count_by

@test.describe("Fixed Tests")
def basic_tests():
    @test.it("Fixed tests")
    def fixed_tests():   
        test.assert_equals(count_by(1, 5), [1, 2, 3, 4, 5])
        test.assert_equals(count_by(2, 5), [2, 4, 6, 8, 10])
```
---

### Given Code


```python
def count_by(x, n):
    """
    Return a sequence of numbers counting by `x` `n` times.
    """

```

---

### my initital Solution


```python
def count_by(x, n):
    output = [] #create blank array
    repeats = 1 # ensure we repeat n times
    while repeats <= n:
        output.append(x * repeats)
        repeats += 1
    return output
    
```

---


[See on CodeWars.com](https://www.codewars.com/kata/5513795bd3fafb56c200049e/train/python)