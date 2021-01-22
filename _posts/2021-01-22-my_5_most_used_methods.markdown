---
layout: post
title:      "My 5 Most Used Methods"
date:       2021-01-22 12:46:23 -0500
permalink:  my_5_most_used_methods
---


1. array.each

This is an obvious one. Often coding challenges have an array that has elements that need to be compared to another piece of data and the most rational way to go about that is .each. With this, one can take each element in an array, in order and apply logic to each of them. 

2. array.each_with_index{ |e, i| ....}

Very similar to each, but one also now has access to the index or placement of each element in the array. This is often able to be used to create a hash with key being the element and the value being the index. In addition, logic can be applied to the order of which the array is in.

3. array.length

This is method that returns the number of elements in an array. I find myself using this for while loops as I shift out elements in an array after applying logic to each element. Here is a brute force example of how I recently found myself using it:

```
def max_profit(prices)
    arr = []
    
    while prices.length > 1
        prices.each_with_index{|e, i| prices.each_with_index{|e2, i2| 
            if i < i2 && e2 - e > 0
                arr << e2 - e
            end}
        }
        prices.shift
    end
    
    if arr.length >= 1
        if arr.sort[-1] > 0
            return arr.sort[-1]
        end
    end
    return 0
end

```

4. array.sort

In the above code I also used the sort method. I often find myself needing to find the largest or smallest number in an array. In order to do that it is easy to find the smallest by using array.sort[0] and the largest by using array.sort[-1].

5. array.map{ |e| ... }

While learning to code I found myself confused with when to use .map compared to .each. Whilst actually coding, I found that the need to mutate the whole array and keep the same name came up frequently. With that, .map is the method used when logic is applied in order to mutate an array, or even create a new array with logic applied to the elements.
