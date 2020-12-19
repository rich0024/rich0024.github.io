---
layout: post
title:      "My First Technical Interview"
date:       2020-12-19 01:22:46 +0000
permalink:  my_first_technical_interview
---


My question:

```
Input:
flight_length
- duration of the flight in minutes
movies
- array of movie times in minutes
Output:
boolean
- true if there exists TWO different movies that add up EXACTLY to the flight_length
Examples:
flight_length - 160
movies - [80, 110, 40]
=> false
[80, 110, 80]
=> true
[20, 30, 110, 40, 50]
=> true
```

How I initially went about the problem:

My first idea was to take each element of the input array with its respective index and compare it to every element of the array that did not share the same index number. In that, I was thinking to set up a while loop with the condition being: if there is  greater than one element in the array.  Within that while loop, I would take the first element then compare it to the other elements by combining the up_to and each method, then shift if all return false. The interviewer told me this is definitely one way to go about the problem but may be more complicated than necessary.

Thus, the interviewer asked if I could think of another way to go about the problem without the while loop or destroying the input array. This was a slight curveball and had to take some time to think. One tip that I received from Flatiron School's project reviews was to take the time to think out loud during technical interviews, so that the reviewer can both understand your thought process and so that the reviewer is aware that you have not completely froze. In that moment I realized that my first idea was a slightly more concise method and that was to take each element and compare with every other element. 

And my answer looked like this:
```
def flight_movies(duration, array)
    array.each_with_index do |arr, i|
        array.each_with_index{|arr2, i2| 
            if i2 != i
                if arr + arr2 == duration
                    return true
                end
            end
        }
    end
    return false
end
```

This was an answer that solved the initial problem and at that moment I thought I succeeded and completely "passed" the technical interview. However, my interviewer explained that this is not the best sollution and that just because two methods may get the same result, it does not make them equal. In that, I had not considered Big O notation. Now, Big O notation deserves its own post, but for now, I shall reference [this](https://www.interviewcake.com/article/python/big-o-notation-time-and-space-complexity) article which my interviewer reccomended. 

After my interviewer explained a simplified version of Big O notation, I had realized why my code was so innefficient. It had to go through the array data and then go through the array data again. With this method, a large array would end up taking a lot of time. Thus, the best sollution would be one with a linear correlation and that uses a hash object.

My feedback was that I had received a 3/5. Now, that is not a passing grade, but there were many things to take away from this interview. Mainly, practice, practice, practice; these questions and syntax will get easier the more one codes, so practice is key. In addition, efficiency in code matters and taking into account Big O notation could give an extra boost. Finally, the positive comments my interviewer left were that I had decent ideas and a positive attitude; attitude can change the tone of the interview and leave a lasting impression.
