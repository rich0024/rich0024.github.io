---
layout: post
title:      "Hash Over Array"
date:       2021-02-06 00:58:31 +0000
permalink:  hash_over_array
---


In my recent coding ventures, I have found myself using hashes instead of arrays. In many ways, hashes are superior than arrays. That is intuitively true, as instead of a single list to work with, there is now a list with an item corresponding with each element, key and value. In application, finding an element becomes easier. 
When looking for a specific element in an array, there are a handful of methods that require specific prior knowledge in order to find said element. Lets take an array that consists of dogs, dogs = [marley, fido, bordeaux, lumi]. With this array, we can use methods like .find_by, .find, dogs[(index #)]. These methods require some prerequisite knowledge so in order to locate an element in this array, the knowledge will need to be very specific like, a dog's index number or details of that dog and would often take lines of logic to be applied on each of the elements in the dog array. 
Now, lets take a hash and have the dog names be the key and index be the value, so it will look something like:
hash = {marley => 0; fido => 1; bordeaux => 2; lumi => 3}
with this, finding the same thing becomes easier and faster. Now, instead of calling a method on an array to find the specific element with a corresponding index, one can simply put hash plus the index and corresponding information will follow "hash[0]" will return marley.
