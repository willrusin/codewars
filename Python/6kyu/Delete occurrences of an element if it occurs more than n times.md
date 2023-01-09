# CodeWars Python Solutions

---

## Delete occurrences of an element if it occurs more than n times


**Definition**

Enough is enough!
Alice and Bob were on a holiday. Both of them took many pictures of the places they've been, and now they want to show Charlie their entire collection. However, Charlie doesn't like these sessions, since the motif usually repeats. He isn't fond of seeing the Eiffel tower 40 times.
He tells them that he will only sit for the session if they show the same motif at most N times. Luckily, Alice and Bob are able to encode the motif as a number. Can you help them to remove numbers such that their list contains each number only up to N times, without changing the order?

Task
Given a list and a number, create a new list that contains each number of list at most N times, without reordering.
For example if the input number is 2, and the input list is [1,2,3,1,2,1,2,3], you take [1,2,3,1,2], drop the next [1,2] since this would lead to 1 and 2 being in the result 3 times, and then take 3, which leads to [1,2,3,1,2,3].
With list [20,37,20,21] and number 1, the result would be [20,37,21].

### Sample Tests]
```Python
test.assert_equals(delete_nth([20,37,20,21], 1), [20,37,21])
test.assert_equals(delete_nth([1,1,3,3,7,2,2,2,2], 3), [1, 1, 3, 3, 7, 2, 2, 2])
```
---

### Given Code


```python
def delete_nth(order,max_e):
    # code here

```

---

### my initital Solution


```python
def delete_nth(order,max_e):
    new_output = list() #blank list
    for i in order:
        if new_output.count(i) < max_e: #if the new list doesnt contain more than max_e occurrences
            new_output.append(i) # add i to the list
    return new_output
```

---


[See on CodeWars.com](https://www.codewars.com/kata/554ca54ffa7d91b236000023/train/python)