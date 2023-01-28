# CodeWars Python Solutions

---

## Find the unique number


**Definition**

There is an array with some numbers. All numbers are equal except for one. Try to find it!

find_uniq([ 1, 1, 1, 2, 1, 1 ]) == 2
find_uniq([ 0, 0, 0.55, 0, 0 ]) == 0.55
It’s guaranteed that array contains at least 3 numbers.

The tests contain some very huge arrays, so think about performance.

This is the first kata in series:

Find the unique number (this kata)
Find the unique string
Find The Unique
]

### Sample Tests]
```Python
try:
    import codewars_test as test
except:
    pass


@test.describe("Basic Tests")
def f():
    @test.it("Simple tests")
    def _():
        test.assert_equals(find_uniq([ 1, 1, 1, 2, 1, 1 ]), 2)
        test.assert_equals(find_uniq([ 0, 0, 0.55, 0, 0 ]), 0.55)
        test.assert_equals(find_uniq([ 3, 10, 3, 3, 3 ]), 10)
```
---

### Given Code


```python
def find_uniq(arr):
    # your code here
    return n   # n: unique number in the array
```

---

### my initital Solution


```python
def find_uniq(arr):
    length = len(arr)
    for i in range(length): ##iterate through the length of the array
        n = arr[i] ##set the answer to the current value
        if i == length - 1: ##if we are at the end just reutrn n
            return n
        else:
            l = (i + 1)
        if i == 0: ##if we are on the first round we cant go back so we go forward over l
            k = i + 2
        else:
            k = (i - 1)
        if n != arr[k] and n != arr[l]:
            return n
        
```

---


[See on CodeWars.com](https://www.codewars.com/kata/585d7d5adb20cf33cb000235/train/python)