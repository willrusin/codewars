# CodeWars Python Solutions

---

## Sum of the first nth term of Series


**Definition**

Task:
Your task is to write a function which returns the sum of following series upto nth term(parameter).

Series: 1 + 1/4 + 1/7 + 1/10 + 1/13 + 1/16 +...
Rules:
You need to round the answer to 2 decimal places and return it as String.

If the given value is 0 then it should return 0.00

You will only be given Natural Numbers as arguments.

Examples:(Input --> Output)
1 --> 1 --> "1.00"
2 --> 1 + 1/4 --> "1.25"
5 --> 1 + 1/4 + 1/7 + 1/10 + 1/13 --> "1.57"

### Sample Tests]
```Python
import codewars_test as test
from solution import series_sum

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(series_sum(1), "1.00")
        test.assert_equals(series_sum(2), "1.25")
        test.assert_equals(series_sum(3), "1.39")
```
---

### Given Code


```python
def series_sum(n):
    # Happy Coding ^_^

```

---

### my initital Solution


```python
def series_sum(n):
    series = [] #create blank array to fill with the fractions
    for n in range(1, 3*n - 1, 3): #generate the fractions with the number generated dependent upon the n value, this way we never get an index out of range
        series.append(1/n)
    return "{:.2f}".format(sum(series))
            #round float the 2 decimal places, as a string.

```

---


[See on CodeWars.com](https://www.codewars.com/kata/57f781872e3d8ca2a000007e)