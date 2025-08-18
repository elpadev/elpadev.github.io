---
layout: post
title: "An intuition of the prefix sum method"
date: 2025-04-16 00:00:00 +0000
categories: algorithms tutorial
---

Imagine you are a runner running a long distance.

There are multiple stages during this long run. The distance between each stage is the same.

During your run, you count how many trees you have seen so far, and at each stage, you write it down.

At the end of your run, you have a list of increasing numbers that show how many trees you had seen by each stage — for example, “2, 5, 6, 9, 10”.

Now the question is: were there any segments with exactly 3 trees?

For each stage, if we subtract 3 from the number of trees we have seen so far at that stage, we should check whether the resulting number is already in our list of notes.

If we have seen 15 trees so far and we want to know if there was a segment with 5 trees, we can check whether there was a stage where we had seen 10 trees.
