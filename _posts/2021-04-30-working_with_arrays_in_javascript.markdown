---
layout: post
title:      "Working with Arrays in Javascript"
date:       2021-05-01 01:21:34 +0000
permalink:  working_with_arrays_in_javascript
---


Most of my coding has been in ruby, but recently I have been working more with javascript. With that, working with arrays are slightly different in order to achieve the same goal.

Push:
- In order to push an item into an array, I like dot notation. 
Example:
`let arr = [1, 2, 3, 4, 5]
		
arr.push('6')`
		
Sort:
- When it comes to sorting in Ruby, '.sort' will already order things from least to most. In Javascript, you need to specify.
Example:
```
let arr = [2, 3, 1, 5, 4]

arr.sort((a, b) => a - b)

//arr now = [1, 2, 3, 4, 5]
```

Navigation:
- If you want to reach the last item in an array in Ruby, you can write array[-1]. However, Javascript does not work the same.
Example
```
let arr = [1, 2, 3, 4, 5]

arr[arr.length -1] //this will return 5

```
