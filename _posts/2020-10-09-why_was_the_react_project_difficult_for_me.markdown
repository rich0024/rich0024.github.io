---
layout: post
title:      "WHY WAS THE REACT PROJECT DIFFICULT FOR ME?"
date:       2020-10-10 03:23:53 +0000
permalink:  why_was_the_react_project_difficult_for_me
---


The final flatiron project, one would think that by this time, the code just flows. However, this project allowed the most freedom and that freedom made the project infinitely more difficult.  In addition, the reqirements for this project were relatively easy to meet and react is able to . With that, the issue was being overloaded with possibilities and react allows for many different ways to reach a goal. Thus,  contrary to previous projects where goals or steps needed to get to the goal were clear, everything was a bit up in the air.

Also, learning and implementing new concepts has been an issue with every project and this project is no different. React initially was easy to conceptualize. I saw it like an elementary school poster project; there was one big poster(container component) and I was glueing cut outs (child components) to the poster. However, this simplification only really applies to static components. With all of the techniques applied, finding something analgous to react is more difficult; maybe it could be seen as a big malll with assistants to help one shop. Even then, that analogy misses concepts of react like state and lifecycles of components.

Coincedentally, state and the lifecyle of components were the most difficult to understand for me. Luckily, in the world of coding, I am not alone and my difficulties are shared with the community. With that, I was one Youtube tutorial away from my 'eureka!' moment. The issue I had was that I was attempting to pull props from state but state was not what I thought it was in that moment. This was due to the lifecycle of components; I was running a function to fetch objects from my server under "componentDidMount()" and setting those objects to state in order to be used by a child component. This did not work because I did not understand the lifecycle of components and that any function under componentDidMount() will run after the whole component mounts. Thus, componentDidMount() occured after the child component was rendered and I was unable to access the objects being retrieved at componentWillMount.

[Here is the video](https://www.youtube.com/watch?v=kVyrzn29QPk&list=PL7pEw9n3GkoVAqCMVTz2mKthyWr-svpQJ&index=9&t=952s) 
