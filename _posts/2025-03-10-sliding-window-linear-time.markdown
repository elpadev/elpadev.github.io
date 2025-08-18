---
layout: post
title: "Why does the sliding window algorithm has linear time complexity?"
date: 2025-03-10 00:00:00 +0000
categories: algorithms tutorial
---

We can imagine the sliding window as a snake eating food items that are in front of it. At each iteration, the snake eats a food item. If the food items currently in its stomach are no longer valid after eating, it has to drop the first food item.

How many food items does the snake eat in total? n food items.

How many food items can it drop at most? n food items.

Thus, the time complexity is O(2n) = O(n).
