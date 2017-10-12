---
title: 'Pythonic: List Comprehension Limits'
date: 2017-09-27 15:45:59
tags: Pythonic
categories: Tech
---

## No More Than Two Expressions In List Comprehension

List comprehension supports multiple loops. For example:

```Python
matrix = [[1,2,3],[4,5,6],[7,8,9]]
flat = [x for row in matrix for x in row]
print (flat)
>>>
[1,2,3,4,5,6,7,8,9]
```

Another example would be creating a two-layer depth new list by inputing list:

```Python
squared = [[x**2 for x in row] for row in matrix]
print(squared)
>>>
[[1,4,9],[16,25,36],[49,64,81]]
```

If there is another loop in expression, list comprehension will become longer. It will be clearer only if splitting it into multiple lines:

```Python
my_lists = [[1,2,3],[4,5,6],...]
flat = [x for sublist1 in my_lists
        for sublist2 in sublist1
        for x in sublist2]
```

From above we can tell that list comprehension under this condition is not simpler than the common way.

Therefore, it is not suggested that using list comprehension with more than two expressions.



