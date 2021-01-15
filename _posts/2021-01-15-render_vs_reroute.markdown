---
layout: post
title:      "Render VS Reroute"
date:       2021-01-15 20:33:22 +0000
permalink:  render_vs_reroute
---


This will be a smaller conceptualization of render compared to reroute in the world of Ruby on Rails. 

In typical MVC style Rails applications, the typical route will match a controller method for routing. However, in some cases, one may not be the correct user to access a certain page or does not have proper information in order to render the proper page. For that instance, we Reroute. For example, you want to access a homepage; however, you are not logged in so you must be rerouted to the login page. The user should only really see the login page, but it took a second to get there compared to just plugging in the login page url. 

Why did it take a little longer? 

In the physical world, I compare this to going to the store for an item. If one goes to the store to get a certain candy bar, but they are all out of that candy bar, one could reroute to the store across the street and get the candy bar there. Thus, the time delay is due to initially attempting to access an item (or erb file) but unable to because of a certaiin circumstance and was directed to another source. 
