---
layout: post
title: "Why should the size of a hash table’s array be a prime number to minimize collisions?"
date: 2025-03-23 00:00:00 +0000
categories: algorithms tutorial
---

Let’s say the index of a hash table’s array is given by `i = h(key) % table_size`.

If `table_size` is 10, then many numbers are divisible by 10, e.g., 10, 20, 30, 40. This means that the index `i` will more often be 0, increasing the probability of collisions.

However, if `table_size` is a prime number, then only a few values of `h(key)` will result in 0—specifically, multiples of the prime number and 0. As a result, the probability of a collision is lower.
