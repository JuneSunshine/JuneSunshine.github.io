---
title: 'Pythonic: Unnecessary Else'
date: 2017-10-04 00:36:38
tags: Pythonic
categories: Tech
---

## Unique Python Else

Python provides a function which is not supported in most of primary languages: To use else statement right behind the loop.

```Python
for i in range(3):
    print ("Loop %s" % i)
else:
    print ("Else what?!")
>>>
Loop 0
Loop 1
Loop 2
Else what?!    
```

You might think this is interesting. 

