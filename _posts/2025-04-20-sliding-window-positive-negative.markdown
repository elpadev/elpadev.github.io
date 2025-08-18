---
layout: post
title: "Sliding window algorithm and mix of positive and negative numbers"
date: 2025-04-20 00:00:00 +0000
categories: algorithms tutorial
---

The sliding window algorithm iterates through the “maximal valid subarray” `[start, end]` (see [Which subarrays does the Sliding Window Algorithm actually visit?](https://elpa.dev/2025/04/14/which-subarrays-does-the-sliding-window-algorithm-actually-visit/)). The problem’s condition is then fulfilled for each subarray starting between `[start, end]` and ending at `end`.

But often the sliding window algorithm doesn’t work if an array contains a mix of positive and negative integers.

This is because the explicitly constructed “maximal valid windows” must contain all valid windows. Not every valid window is constructed explicitly; that’s why the algorithm is so efficient.

Let’s say the task is to get the longest subarray with a max sum of `X`. At one of the iterations, the “maximal valid window” `[start, end]` is constructed. Then, each subarray starting between `[start, end]` and ending at `end` must also be valid.

But if this window has a negative number, then removing that number is like adding a positive number, which could lead the sum to be greater than `X`.
