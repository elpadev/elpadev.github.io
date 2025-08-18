---
layout: post
title: "Does the Sliding Window Technique Visit Every Valid Subarray?"
date: 2025-04-14 00:00:00 +0000
categories: algorithms tutorial
---

In the sliding window technique, we do not go through every possible subarray. This is what makes the technique so efficient.

But do we go through every valid subarray (as defined by the problem)?

No, the sliding window technique doesn’t even go through every valid solution!

But are all valid subarrays somehow included in the windows that we explicitly visit?

Yes!

If you take all the windows that are explicitly generated, you can do something to get all the valid subarrays.

Let’s say we explicitly visit a window `[left, right]`.

Every subarray that starts somewhere between `left` and `right`, and ends at `right`, is a valid subarray!

So, if you go through all the generated windows and build subarrays in this way, you will get all the valid subarrays!
