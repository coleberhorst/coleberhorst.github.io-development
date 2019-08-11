---
layout: post
title: "Python Exercism"
date: 2019-06-14
description: 
image: /assets/images/exercism.jpg
author: Cole Berhorst
tags:
  - Squid
---
Finished the [Exercism](https://exercism.io/tracks/python) python exercises. I did this as practice to keep my python skills sharp.

## What I learned
I loved the do-it-yourself approach where you had to self-learn at times to solve problems. The community solutions were also very helpful: sometimes my solutions were unique and very efficient, and sometimes a community memeber's solution taught me a whole new way of looking at the problem.

```python
def is_equilateral(sides):
    return len(set(sides)) == 1 and is_triangle(sides)
    
def is_isosceles(sides):
    return len(set(sides)) < 3 and is_triangle(sides)
    
def is_scalene(sides):
    return len(set(sides)) == 3 and is_triangle(sides)

def is_triangle(sides):
    return all(sides) and 2*max(sides) < sum(sides)
```

# Testing at forefront
The best part was that testing was required from the beginning as that is how solutions are solved.

```python
class RunLengthEncodingTest(unittest.TestCase):
    def test_encode_empty_string(self):
        self.assertMultiLineEqual(encode(''), '')
```

Though sometimes I felt pressured to make solutions shorter which is something I could work on. The below code solves all the tests, but is not very accessible for later review.

```python
def is_armstrong(number):
    return number == sum([pow(int(x),len(str(number))) for x in str(number)])
```

My solutions are hosted on [Github](https://github.com/coleberhorst/python-exercism).


