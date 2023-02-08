# CodeWars Python Solutions

---

## Who likes it?


**Definition**
You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

[]                                -->  "no one likes this"
["Peter"]                         -->  "Peter likes this"
["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"
Note: For 4 or more names, the number in "and 2 others" simply increases.
]

### Sample Tests]
```Python
import codewars_test as test
from solution import likes

@test.it('Basic tests')
def _():
    test.assert_equals(likes([]), 'no one likes this')
    test.assert_equals(likes(['Peter']), 'Peter likes this')
    test.assert_equals(likes(['Jacob', 'Alex']), 'Jacob and Alex like this')
    test.assert_equals(likes(['Max', 'John', 'Mark']), 'Max, John and Mark like this')
    test.assert_equals(likes(['Alex', 'Jacob', 'Mark', 'Max']), 'Alex, Jacob and 2 others like this')
```
---

### Given Code


```python
def likes(names):
    # code here
pass
```

---

### my initital Solution


```python
def likes(names):
    # your code here
    num = len(names)
    result = ""
    #check for empty list
    if not num:
        result = "no one likes this"
        return result
    else:
        if num == 1:
            result = ("{} likes this".format(names[0]))
            return result
        elif num == 2:
            result = "{} and {} like this".format(names[0], names[1])
            return result
        elif num == 3:
            result = "{}, {} and {} like this".format(names[0], names[1], names[2])
            return result
        else:
            result = "{}, {} and {} others like this".format(names[0], names[1], (num - 2))
            return result
   
    
```

---


[See on CodeWars.com](https://www.codewars.com/kata/5266876b8f4bf2da9b000362/train/python)