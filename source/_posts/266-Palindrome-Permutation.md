---
title: 266. Palindrome Permutation
date: 2017-08-28 12:31:45
tags: Leetcode
categories: Tech
---

## Problem
>Given a string, determine if a permutation of the string could form a palindrome.

>For example,
"code" -> False, "aab" -> True, "carerac" -> True.

<!--more-->

## Solution

1. ##### Common
The most common way to solve this problem will be using stack. If a new letter is found, push it into the stack, then pop it out whenever it appears the second time. 

2. ##### Optimized
Using dictionary will be the best solution. Store each letter as a key and the value is the count of its appearance. It is a little faster in this way because the time complexity of search is O(1).

Python code link:
https://github.com/JuneSunshine/Optimized_Leetcode_Solution/blob/master/Palindrome_Permutation.py

