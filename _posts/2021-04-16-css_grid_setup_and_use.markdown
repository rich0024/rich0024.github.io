---
layout: post
title:      "CSS Grid Setup and Use"
date:       2021-04-16 19:05:07 +0000
permalink:  css_grid_setup_and_use
---


Getting code to work and be functional is its own challenge. After getting everything working and styled, similar to realestate, one must think "location, location, location". Design is a challenging part for many developers  and is  often overlooked.  Thus, a few of us are guilty  of  ignoring some CSS techniques. The grid is a simple way to start the placement of divs.

Grid is exactly what one would think, a grid. This simplicity  makes it easy to  work  with. Here is how  to set  up and  use a  grid.

 First, set up  the  parameters of the grid, how  many  columns and rows.  Here is a 2x2 grid:
```
.main {
    height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
}
```

Now, in order to place a div within the grid add the following code to the "main" styling:
```
    grid-template-areas:
        "box1 box2"
        "box3 box3";
```

 what is box1, box2 and box3? They  are  whatever you  assign  them to be. Here  is  how  to  assign  them:
```

.desktop-4 {
    grid-area: box2;
}
```

Within any div styling, use 'grid-area:' then assignna variable name. Then, the div will be placed where it was originally mapped in accordance with "grid-template-areas:'
