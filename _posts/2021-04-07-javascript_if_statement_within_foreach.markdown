---
layout: post
title:      "Javascript If Statement Within forEach"
date:       2021-04-07 16:48:43 +0000
permalink:  javascript_if_statement_within_foreach
---


Recently, I have been practicing some algorithms in Javascript. Previously, I did algorithm questions in ruby; so, now I have to reorient the way I can use methods and iterations. Within ruby, using an if statement within a .each method is pretty straightforward. However, in javascript, it is a bit complicated. According  to Michael Lehenbauer on StackOverflow, "your forEach callback can return true to cancel enumeration and forEach() will return true to signal that enumeration was canceled." With that, we have to switch up the logic a bit. I found that using "for" loops works will.

Here is my answer for the algorithm I was working on:
```
function twoNumberSum(array, targetSum) {
  // Write your code here.
	const nums = {}
	for (const num of array) {
		const ans = targetSum - num;
		if (ans in nums) {
			return [ans, num];
		}
		else {
			nums[num] = true;
		}
	}
	return []
}
```

On line 4 there are two things to take not of: 'const num of array' means you are setting a variable, num for each element of an array; and the for loop can accept that as its condition.
