# CodeWars Python Solutions

---

## Mexican Wave


**Definition**

The wave (known as the Mexican wave in the English-speaking world outside North America) is an example of metachronal rhythm achieved in a packed stadium when successive groups of spectators briefly stand, yell, and raise their arms. Immediately upon stretching to full height, the spectator returns to the usual seated position.

The result is a wave of standing spectators that travels through the crowd, even though individual spectators never move away from their seats. In many large arenas the crowd is seated in a contiguous circuit all the way around the sport field, and so the wave is able to travel continuously around the arena; in discontiguous seating arrangements, the wave can instead reflect back and forth through the crowd. When the gap in seating is narrow, the wave can sometimes pass through it. Usually only one wave crest will be present at any given time in an arena, although simultaneous, counter-rotating waves have been produced. (Source Wikipedia)
Task
In this simple Kata your task is to create a function that turns a string into a Mexican Wave. You will be passed a string and you must return that string in an array where an uppercase letter is a person standing up. 
Rules
 1.  The input string will always be lower case but maybe empty.

 2.  If the character in the string is whitespace then pass over it as if it was an empty seat
Example
wave("hello") => ["Hello", "hEllo", "heLlo", "helLo", "hellO"]
Good luck and enjoy!

### Sample Tests]
```Python
from solution import wave
import codewars_test as test

import random

@test.describe('Testing')
def example_tests():
    
    @test.describe('Example tests')
    def example_tests():

        result = ["Hello", "hEllo", "heLlo", "helLo", "hellO"]
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case1():
            test.assert_equals(wave("hello"), result)

        result = ["Codewars", "cOdewars", "coDewars", "codEwars", "codeWars", "codewArs", "codewaRs", "codewarS"]
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case2():
            test.assert_equals(wave("codewars"), result)

        result = []
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case3():
            test.assert_equals(wave(""), result)

        result = ["Two words", "tWo words", "twO words", "two Words", "two wOrds", "two woRds", "two worDs", "two wordS"]
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case4():
            test.assert_equals(wave("two words"),result)

        result = [" Gap ", " gAp ", " gaP "]
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case5():
            test.assert_equals(wave(" gap "), result)

        result = ["A       b    ", "a       B    "]
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case6():
            test.assert_equals(wave("a       b    "), result)

        result = ["This is a few words", "tHis is a few words", "thIs is a few words", "thiS is a few words", "this Is a few words", "this iS a few words", "this is A few words", "this is a Few words", "this is a fEw words", "this is a feW words", "this is a few Words", "this is a few wOrds", "this is a few woRds", "this is a few worDs", "this is a few wordS"]
        @test.it("Should return: '["+", ".join(result)+"]'")
        def example_test_case7():
            test.assert_equals(wave("this is a few words"), result)

```
---

### Given Code


```python
def wave(people):
    # Code here
    pass

```

---

### my initital Solution


```python
def wave(people):
    people = people.lower() #start with lowercase
    mwave = [] #blank array
    for n,i in enumerate(people): #enumerate with n as index and i as character
        if i == " ": #cater for space
            continue
        else:
            mwave.append(people[:n] + people[n].upper() + people[n+1:])
#append from the first character to e index, switch e to upper, increment e
    return mwave

```

---


[See on CodeWars.com](https://www.codewars.com/kata/554ca54ffa7d91b236000023/train/python)