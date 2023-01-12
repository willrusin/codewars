# CodeWars Python Solutions

---

## Build a tower


**Definition**

Build a pyramid-shaped tower, as an array/list of strings, given a positive integer number of floors. A tower block is represented with "*" character.

For example, a tower with 3 floors looks like this:

[
  "  *  ",
  " *** ", 
  "*****"
]
And a tower with 6 floors looks like this:

[
  "     *     ", 
  "    ***    ", 
  "   *****   ", 
  "  *******  ", 
  " ********* ", 
  "***********"
]

### Sample Tests]
```Python
import codewars_test as test
from solution import tower_builder

@test.describe("Build Tower")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(tower_builder(1), ['*', ])
        test.assert_equals(tower_builder(2), [' * ', '***'])
        test.assert_equals(tower_builder(3), ['  *  ', ' *** ', '*****'])
```
---

### Given Code


```python
def tower_builder(n_floors):
    # build here

```

---

### my initital Solution


```python
def tower_builder(n_floors):
    tower = [] #new blank "tower" to build
    width = (n_floors * 2) - 1 #number of * will alwaysbe odd
    for b in range(1, 2 * n_floors, 2): #range will always be min 1 up to double number of floors, only take odd numbers.
        bricks = b * '*' 
        line = bricks.center(width) #use .center to format the tower
        tower.append(line)
    return tower
    
```

---


[See on CodeWars.com](https://www.codewars.com/kata/576757b1df89ecf5bd00073b/train/python)