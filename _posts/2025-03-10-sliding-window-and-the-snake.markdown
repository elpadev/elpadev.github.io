---
layout: post
title: "Sliding window and the snake"
date: 2025-03-10 10:00:00 +0000
categories: algorithms explanation
---

Imagine a snake with an array of food items in front of it. The snake can eat a food item only if a certain condition is met.

The sliding window represents the snake. The window attempts to "eat" a new piece of food, but it can do so only if a specific condition allows it. If the condition is not met, the snake must drop the first item in its stomach before consuming the new one.

Let's consider this array: `[3, 5, 1, 3, 2]`. Our goal is to find the largest subarray whose sum is less than 10. Here’s how the sliding window progresses:

- `[**3** , 5, 1, 3, 2]` → The snake eats the first element. The sum of the foods in the stomach is within the limit, so the snake can eat the next item.
- `[**3, 5** , 1, 3, 2]` → The sum is within the limit, so we add the next element.
- `[**3, 5, 1** , 3, 2]` → If the snake would "eat" the 3, the sum would exceed 10. So it "drops" the first element in the window and "eats" the next one.
- `[3, **5, 1, 3** , 2]` → If it would eat the "2", the sum would exceed 10. So it "drops" the first element in the window and "eats" the next one.
- `[3, 5, **1, 3, 2**]` → Now, all “food items” are “eaten”. So we are done.