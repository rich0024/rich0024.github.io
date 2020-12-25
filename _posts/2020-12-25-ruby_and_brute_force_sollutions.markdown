---
layout: post
title:      "Ruby and Brute Force Sollutions"
date:       2020-12-25 20:16:13 +0000
permalink:  ruby_and_brute_force_sollutions
---


For my recent technical interview and a few coding questions I have been working on, I realize that I am taking the same approach. My way of thinking has been to create a set of rules to follow with a bunch of while loops and if statements. Although, not often the most efficient, it is effective and has a few benefits.

One of my early views on coding was that coding is similar to legos; small pieces that fit together a certain way to eventually build a structure. Thinking back, this is an oversimplification that holds some truth. This all seems abstract, but I would like to keep track of some of these thoughts and watch them evolve. 

Some examples of how I have used brute force coding sollutions

Question:
> Given a sequence of integers as an array, determine whether it is possible to obtain a strictly increasing sequence by removing no more than one element from the array.

My answer:
```
def almostIncreasingSequence(sequence)
#looking to make check if the first is less than the next. then, continue to check.
    arr2 = []

    while sequence.length > 2
        if sequence[0] < sequence[1] && sequence[0] < sequence[2]
            sequence.shift
        elsif sequence[0] >= sequence[1] && sequence[0] < sequence[2]
            arr2 << sequence[1]
            sequence.delete_at(1)
        elsif sequence[0] < sequence[1] && sequence[0] >= sequence[2]
            arr2 << sequence[2]
            sequence.delete_at(2)
        else
            arr2 << sequence[0]
            sequence.shift
        end
    end
    
    if sequence.length == 2 && sequence[0] >= sequence[1]
        arr2 << sequence[0]
        sequence.shift  
    else
        nil
    end
        
    
    
    if arr2.length >= 2
        return false
    else
        return true
    end

end
```

With this answer, I did not take Big O notation into acount, so this is definitely not the most efficient code. However, it is okay to get something to work and then break things down to something more efficient. For this, my initial thought was to isolate what needs to be compared and the to put what does not fit into an array. If there were too many items that did not fit then there would be a return of false.
