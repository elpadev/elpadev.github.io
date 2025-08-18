---
layout: post
title: "Which subarrays are counted by the prefix sum method?"
date: 2025-04-16 00:00:00 +0000
categories: algorithms tutorial
---

The prefix sum method is efficient because it doesn’t iterate through every possible subarray.

Instead, at each iteration, it asks the question: Have we seen a subarray that fulfills the condition and ends at the current index?

At each iteration, it counts the number of valid subarrays that end at the current index.
