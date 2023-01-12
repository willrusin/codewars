# CodeWars Python Solutions

---

## Transportation on vacation


**Definition**

After a hard quarter in the office you decide to get some rest on a vacation. So you will book a flight for you and your girlfriend and try to leave all the mess behind you.

You will need a rental car in order for you to get around in your vacation. The manager of the car rental makes you some good offers.

Every day you rent the car costs $40. If you rent the car for 7 or more days, you get $50 off your total. Alternatively, if you rent the car for 3 or more days, you get $20 off your total.

Write a code that gives out the total amount for different days(d).

### Sample Tests]
```Python
import codewars_test as test
from solution import rental_car_cost

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(rental_car_cost(1),40)
        test.assert_equals(rental_car_cost(4),140)
        test.assert_equals(rental_car_cost(7),230)
        test.assert_equals(rental_car_cost(8),270)

```
---

### Given Code


```python
def rental_car_cost(d):
    # your code

```

---

### my initital Solution


```python
    def rental_car_cost(d):
    total = d * 40
    if d >= 3 and d < 7: #check for minimum 3 days but less than 7 for $20 discount
        total -= 20
        return total
    elif d >= 7: #check for 7 or more days for $50 discount
        total -= 50
        return total
    else: #else its less than 3 days so no discount.
        return total
```

---


[See on CodeWars.com](https://www.codewars.com/kata/568d0dd208ee69389d000016/train/python)