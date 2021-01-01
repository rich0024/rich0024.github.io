---
layout: post
title:      "Creating a Slot Machine With React"
date:       2021-01-01 17:56:58 +0000
permalink:  creating_a_slot_machine_with_react
---


Recently, I have been tasked with creating a slot machine web app using react and redux for the front end. Before starting, I would like to blog out the planning process and layout any questions I may have in the future. My planning process goes as followed: function (what is the goal of the app), breakdown and structure (folder structure and architecture). Along the way, I also like to write out possible challenges I will come across.

Function:
Push a button, randomly select an element from each array(3), if two or three elements in a row match, issue payout.

Breakdown:
* User will need a balance
* Button that trigger an on click event
           * Event, randomly select element from each array 
           * If element arr1 == arr2 != arr3 || arr1 != arr2 == arr3, then smaller payout (not actual code)
           * If  element arr1 == arr2 == arr3, then big payout (not actual code)
           * if  element arr1 != arr2 != arr3 then no payout (not actual code)
           * "Payout" will add to balance
           * Triggering event will take from balance, regardless of result
           * Reset slot machine
    
Structure:
       Components: balance, button, slots, user profile card?, rules section?, home page?, empty balance?

Challenges:
* Logic of reading and paying out
* How to give the slot effect where it looks like the array is rolling
* Timing, each array should roll sequencely
* Aesthetics
* Big display of winning
