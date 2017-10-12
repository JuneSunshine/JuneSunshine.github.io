---
title: 1. Two Sum
date: 2017-08-16 10:33:18
tags: Leetcode
categories: Tech
---

## Problem
>Given an array of integers, return indices of the two numbers such that they add up to a specific target.

>You may assume that each input would have exactly one solution, and you may not use the same element twice.

>Example:
Given nums = [2, 7, 11, 15], target = 9,

>Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

<!-- more -->

## Solution
This appears to be the first and easiest problem on Leetcode. Most people will use the brute force way to solve this problem. However, it is not time efficient.

The best way to solve this is using dictionary which means the time efficiency of checking is O(1). Each time a new number is found, it will be added in the dictionary as value while the key is the difference between this number and target.

Python code link:
<https://github.com/JuneSunshine/Optimized_Leetcode_Solution/blob/master/twoSum.py>


