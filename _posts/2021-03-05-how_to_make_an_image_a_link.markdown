---
layout: post
title:      "How to Make an Image a Link"
date:       2021-03-06 00:28:22 +0000
permalink:  how_to_make_an_image_a_link
---


In an earlier blog I discussed how to add an image to a react project. Now, here is a quick tid bit on how to make an image a link. This can be useful for portfolio projects or linking social media to a website.

-First, add the image as previously discussed in an image tag like so:
```
            <div>
                <img src={cropped}></img>
            </div>
```

-Then, create an a tag with the href link around the image tag.
```
            <div>
						    <a href="whatever link">
                <img src={cropped}></img>
								</a>
            </div>
```
 
 That is all; now if the image is clicked, one will be redirected to the link.
