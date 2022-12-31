# CodeWars Python Solutions

---

## Count of positives / sum of negatives


**Definition**

DESCRIPTION:
Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.

If the input is an empty array or is null, return an empty array.

Example
For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

### Sample Tests]
```Python
import codewars_test as test
from solution import count_positives_sum_negatives

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(count_positives_sum_negatives([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15]),[10,-65])
        test.assert_equals(count_positives_sum_negatives([0, 2, 3, 0, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14]),[8,-50])
        test.assert_equals(count_positives_sum_negatives([1]),[1,0])
        test.assert_equals(count_positives_sum_negatives([-1]),[0,-1])
        test.assert_equals(count_positives_sum_negatives([0,0,0,0,0,0,0,0,0]),[0,0])
        test.assert_equals(count_positives_sum_negatives([]),[])

@test.describe("Random Tests")
def random_tests():
    
    from random import randint
    from functools import reduce
    
    sol=lambda arr: reduce(lambda a,b: [a[0]+1 if b>0 else a[0],a[1]+b if b<0 else a[1]], arr, [0,0])

    for _ in range(40):
        arr=[randint(-100,100) for q in range(randint(1,100))]
        @test.it(f"Testing for count_positives_sum_negatives({arr})")
        def test_case():
            expected = sol(arr)
            test.assert_equals(count_positives_sum_negatives(arr), expected,"It should work for random inputs too")
```
---

### Given Code


```python
def count_positives_sum_negatives(arr):
    # your code here
    pass
```

---

### my initital Solution


```python
def count_positives_sum_negatives(arr):
    pos = []
    if arr:
        pos = [0,0]
    for i in arr:
        if i > 0:
            pos[0] += 1
        elif i < 0:
            pos[1] += i
    return pos
```

---


[See on CodeWars.com](https://www.codewars.com/kata/576bb71bbbcf0951d5000044)