# CodeWars Python Solutions

---

## Lost without a map


**Definition**

Given an array of integers, return a new array with each value doubled.

For example:

[1, 2, 3] --> [2, 4, 6]

### Sample Tests]
```Python
# New tests for 3.8+
import codewars_test as test
from solution import maps

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        tests = [
            [[1, 2, 3], [2, 4, 6]],
            [[0, 1, 2, 3, 4, 5, 6, 7, 8, 9], [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]],
            [[], []]
        ]
        
        for inp, exp in tests:
            test.assert_equals(maps(inp), exp)
    

@test.describe("Random Tests")
def random_tests():

    from random import randint
    
    reference = lambda a: [e * 2 for e in a]
    
    for _ in range(100):
        test_case = [randint(-1000, 1000) for i in range(randint(1, 1000))]
        @test.it(f"testing for maps({test_case})")
        def test_case():
            test.assert_equals(maps(test_case[:]), reference(test_case[:]))
```
---

### Given Code


```python
def maps(a):
    # your code here

```

---

### my initital Solution


```python
def maps(a):
    arr_d = []
    for i in a:
        arr_d.append(i * 2)
    return arr_d
```

---


[See on CodeWars.com](https://www.codewars.com/kata/57f781872e3d8ca2a000007e)