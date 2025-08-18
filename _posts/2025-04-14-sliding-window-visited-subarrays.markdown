---
layout: post
title: "Which subarrays does the Sliding Window Algorithm actually visit?"
date: 2025-04-14 00:00:00 +0000
categories: algorithms tutorial
---

In the sliding window technique, we do not iterate through each possible subarray. This is why the algorithm is so efficient!

But we do iterate through some subarrays!

The question is: which subarrays do we iterate through?

At each iteration, the current window is `[left, right]`. We shrink the window by moving `left`, until the window is valid.

So we can say that at each iteration, the window is the largest possible valid window that ends at `right`. If we increased the size of the window (as `right` is fixed, we would have to move `left`), the window would no longer be valid.

So we can say that at each iteration, we create a valid window that is the largest possible valid window that ends at `right`.
