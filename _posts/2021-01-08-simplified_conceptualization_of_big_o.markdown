---
layout: post
title:      "Simplified Conceptualization of Big O"
date:       2021-01-08 21:09:03 +0000
permalink:  simplified_conceptualization_of_big_o
---


It is a big moment to get to the technical interview stage; it is exciting and nerve wracking at the same time. The initial step after getting the question is to think things out and figure out how to solve the question. Then, after communicating the thought process and finally getting the code to solve the problem, is that it?  Nope, the next question to ask yourself is, "is this the most efficient answer?" We now must consider Big O notation.

Intuitively, one can somewhat conceptualize Big O. How I conceptualize it is imagining things in physical space.  Hypothetically, before cell phones, lets say your friend goes to a vending machine and asks if you want anything and you respond, "a candy bar". Your friend gets to the machine and sees a bunch of candy bars; not knowing which candy bar you want, he walks back to you and asks what kind and you respond a hershey. Your friend goes back and they do not see a hershey... this is getting inefficient. How does one make this more efficient? Let's answer that with Big O terminology.

O(n^2) can be seen as the way you and your friend were originally trying to solve the problem. You have an array of candy you like, and your friend is taking one element from your array and iterating over the vending machine array. Then if the element does not match, your friend asks for your next pick and repeats this process until you get a candy you like. 

O(n) can be seen as your friend going to the vending machine, not seeing what you like, then writing down/memorizing the candy bars they do have. Then they go back to you and you choose from the list your friend gives you.

O(1) can be seen as when your friend asks, what you would like, you give a list of candy bars you like and say if they don't have any of them then you do not want anything.

This is a simplified version of Big O and lacks an example for O(log n). However, it is easy to conceptualize the fastest way to get you a desired candy bar. Thus, when concepualizing coding questions, one can ask themselves "how many times do I have to iterate over an array?" or "can i make an object (similar to the list you gave your friend) to make things more efficient?"
