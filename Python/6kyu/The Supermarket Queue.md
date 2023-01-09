# CodeWars Python Solutions

---

## The Supermarket Queue


**Definition**

There is a queue for the self-checkout tills at the supermarket. Your task is write a function to calculate the total time required for all the customers to check out!

input
customers: an array of positive integers representing the queue. Each integer represents a customer, and its value is the amount of time they require to check out.
n: a positive integer, the number of checkout tills.
output
The function should return an integer, the total time required.

Important
Please look at the examples and clarifications below, to ensure you understand the task correctly :)

Examples
queue_time([5,3,4], 1)
# should return 12
# because when n=1, the total time is just the sum of the times

queue_time([10,2,3,3], 2)
# should return 10
# because here n=2 and the 2nd, 3rd, and 4th people in the 
# queue finish before the 1st person has finished.

queue_time([2,3,10], 2)
# should return 12
Clarifications
There is only ONE queue serving many tills, and
The order of the queue NEVER changes, and
The front person in the queue (i.e. the first element in the array/list) proceeds to a till as soon as it becomes free.
N.B. You should assume that all the test input will be valid, as specified above.

P.S. The situation in this kata can be likened to the more-computer-science-related idea of a thread pool, with relation to running multiple processes at the same time: https://en.wikipedia.org/wiki/Thread_pool

### Sample Tests]
```Python
test.assert_equals(queue_time([], 1), 0, "wrong answer for case with an empty queue")
test.assert_equals(queue_time([5], 1), 5, "wrong answer for a single person in the queue")
test.assert_equals(queue_time([2], 5), 2, "wrong answer for a single person in the queue")
test.assert_equals(queue_time([1,2,3,4,5], 1), 15, "wrong answer for a single till")
test.assert_equals(queue_time([1,2,3,4,5], 100), 5, "wrong answer for a case with a large number of tills")
test.assert_equals(queue_time([2,2,3,3,4,4], 2), 9, "wrong answer for a case with two tills")

# add your own test cases here

```
---

### Given Code


```python
def queue_time(customers, n):
    # TODO  

```

---

### my initital Solution


```python
def queue_time(customers, n):
    # order doesnt change, no optimisation
    co = [0]*n #create list of checkouts (n)
    for i in customers: #iterate over times (customers)
      co[0] += i #add the time to the next available CO
      co.sort() #sort to get the next available CO
    return max(co) #return max time across all COs as this will be the total time

```

---


[See on CodeWars.com](https://www.codewars.com/kata/57b06f90e298a7b53d000a86/train/python)