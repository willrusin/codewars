# CodeWars Python Solutions

---

## Disemvowel Trolls


**Definition**

Trolls are attacking your comment section!

A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat.

Your task is to write a function that takes a string and return a new string with all vowels removed.

For example, the string "This website is for losers LOL!" would become "Ths wbst s fr lsrs LL!".

Note: for this kata y isn't considered a vowel.

### Sample Tests]
```Python
import codewars_test as test
from solution import disemvowel

@test.describe("Fixed Tests")
def basic_tests():
    @test.it("First fixed test")
    def fixed_test_1():
        test.assert_equals(disemvowel("This website is for losers LOL!"), "Ths wbst s fr lsrs LL!")
```
---

### Given Code


```python
def disemvowel(string_):
    return string_

```

---

### my initital Solution


```python
def disemvowel(string_):
    return (string_.translate({ord(i): None for i in 'aeiouAEIOU'}))
#translate example taken from https://www.digitalocean.com/community/tutorials/python-remove-character-from-string

```

---


[See on CodeWars.com](https://www.codewars.com/kata/52fba66badcd10859f00097e/python)