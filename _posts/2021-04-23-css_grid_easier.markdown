---
layout: post
title:      "CSS Grid Easier"
date:       2021-04-23 16:26:14 +0000
permalink:  css_grid_easier
---


Woah! I think I stumbled upon something. I was working with my portfolio and setting up a grid display, getting slightly frustrated. Setting up a 2x2 grid worked easily as I described in my previous post. However, I wanted to get weird and try a 9x9 grid. I set up everything similar to a YouTube tutorial, but everything was going to the top left of the page.

I attempted to change my grid setup many times using: grid-area, adjusting template columns and rows, changing syntax from 1 fr to 'repeat(9, 1fr)' and more. What did work was actually to delete the template rows and columns set up, but keeping the grid area. 

Here is the code:
```
.main {
    display: grid;
    height: 100vh;
    grid-template-areas:
        ". . . . . . ."
        ". . box1 box2 box2 . ."
        ". . box1 box2 box2 . ."
        ". box3 box3 box3 box3 box3 ."
        ". . . . . . .";
}
```

