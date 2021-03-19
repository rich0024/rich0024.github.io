---
layout: post
title:      "Centering with CSS"
date:       2021-03-19 16:19:05 +0000
permalink:  centering_with_css
---


No matter how functional and amazing a project is, nobody will care if it doesn't look good. As I learned to code, I was very focused on function and I settled for the simplest styling. Most of my styling was limited to centering everything and changing the background color. My thought process was that there are templates that could handle all the styling I need. However, to call myself a "fullstack" developer, I better be able to display frontend skills. Oh wait, because I neglected styling so long, I found that styling is not as easy as I thought. I also found that even centering things is slightly more complicated than I assumed. 

To center everything, I used to use the following code:
```
body {
     align-content: center;
}
```

Now, I thought this logic would work for pretty much every <div>. However, "align-content: center" or "align-self: center" does not work for everything. Actaully, it does not work most of the time. Lets take a nav bar or if you look to the top of this blog, there's a home and about link. If we wanted to center those links, "align-content: center" does not seem to center them. I found that "justify-content: center" works better.

Example:
```
.collapse navbar-collapse {
      justify-content: center
}
```
