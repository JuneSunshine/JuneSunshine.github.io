---
title: 'Pythonic: List Comprehension'
date: 2017-09-26 21:33:32
tags: Pythonic
categories: Tech
---

## Better if List Comprehension else Map and Filter

List comprehension is a simple way provided by Python to make another list based on one list.

```Python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squares = [x**2 for x in a]
print(squares)
>>>
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

Unless it is a function with only one parameter, list comprehension is much clearer than 'map'.

```Python
squares = map(lambda x: x**2, a)
```

List comprehension will filter out the elements in original list so that the generated list does not conclude corresponding computational results. For example:

```Python
even_squares = [x**2 for x in a if x % 2 == 0]
print (even_squares)
>>>
[4, 16, 36, 64, 100]
```

Of course, the combination of filter and map functions can do the work too, but the code will be harder to read.

```Python
alt = map(lambda x: x**2, filter(lambda x: x % 2 == 0, a)
assert even_squares == list(alt)
```

The last thing to mention is that dict and set also have similar mechanism with list. We can use this while writing algorithms.

```Python
club_ranks = {'Chelsea': 1, 'Man United': 2, 'Liverpool': 3}
rank_dict = {rank: name for name, rank in club_ranks.items()}
club_len_set = {len(name) for name in rank_dict.values()}
print (rank_dict)
print (club_len_set)
>>>
{1: 'Chelsea', 2: 'Man United', 3: 'Liverpool'}
{7, 10, 9}
```


## Key Points

* List comprehension is clearer than built-in map and filter functions
* List comprehension can skip inputing some elements in list, it can also be done by map but only if combined with filter
* Dict and set also support comprehension

