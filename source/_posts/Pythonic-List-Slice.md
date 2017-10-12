---
title: 'Pythonic: List Slice'
date: 2017-10-07 15:30:29
tags: [Pythonic, List]
categories: Tech
---

## Fundamentals
There are three different parts of list slice operation: start, end, stride.

For easier understanding, we can imagine a whole list is represented as alist[::].

```Python
alist = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']

# assume alist[a:b:c]
# a - start
# b - end
# c - stride
# As default, a is 0, b is len(alist) and c is 1 if we don't assign 
# any of them a number. Therefore, we usually leave the space if we 
# want default values. As follows:

assert alist == alist[::]
assert alist[:3] == alist[0:3] 
assert alist[3:] == alist[3:len(alist)]
```

If we want to start counting from the end, negative values can be used to do the job.

```Python
a[:]        # ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
a[:5]       # ['a', 'b', 'c', 'd', 'e']
a[:-1]      # ['a', 'b', 'c', 'd', 'e', 'f', 'g']
a[4:]       #                     ['e', 'f', 'g']
a[-3:]      #                          ['f', 'g', 'h']
a[2:5]      #           ['c', 'd', 'e']
a[2:-1]     #           ['c', 'd', 'e', 'f', 'g']
a[-3:-1]    #                          ['f', 'g']
```

Even if number out of index, there won't be an issue during list slicing. On the contrary, it will throw exception during visiting single element.

What need to be paid attention to is that a new list will be created after slicing the original list. It means the system is still maintaining the reference towards each object in original list. Therefore, any modifications and changes made on the new list after list slicing will not affect original list. For example:

```Python
b = a[:4]
print ("Before:   ", b)
b[0] = 'z'
print ("After:    ", b)
print ("Original: ")

>>>
Before:   ['a', 'b', 'c', 'd']
After:    ['z', 'b', 'c', 'd']
Original: ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
```

<!-- more -->

