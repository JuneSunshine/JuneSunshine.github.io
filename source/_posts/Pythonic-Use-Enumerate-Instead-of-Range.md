---
title: 'Pythonic: Use Enumerate() Instead of Range()'
date: 2017-10-03 14:19:34
tags: Pythonic
categories: Tech
---

## Try enumerate() more

When iterating through integers, the built-in range function is useful:

```Python
for i in range(10):
    print (i)
```

For strings, we can directly iterate through the list:

```Python
club_list = ['Chelsea', 'Liverpool', 'Barcelona', 'Juventus']
for club in club_list:
    print ("%s is the best!" % club)
```

Sometimes we want to know the index of current element in list while iterating. For example, print the ordered list of football clubs:

```Python
for i in range(len(club_list)):
    club = club_list[i]
    print ("%d: %s" % (i+1, club))
```

However, this method seems a little redundant and also hard to understand. In this situation, Python provides a built-in function: enumerate(). It is a simpler and more elegant way to deal with this.

```Python
for i, club in enumerate(club_list):
    print ("%d: %s" % (i+1, club))
>>>
1: Chelsea
2: Liverpool
3: Barcelona
4: Juventus    
```

We can even assign the starting value of counting, which will make the code even simpler:

```Python
for i, club in enumerate(cub_list, 1):
    print ("%d: %s" % (i, club))
```

## Key Points:

* enumerate() offers a simple way of retrieving each element's index during iteration
* Try to use enumerate() to replace range() if index is needed
* We can use a second parameter in enumerate() to assign the starting value of index (0 as default)

