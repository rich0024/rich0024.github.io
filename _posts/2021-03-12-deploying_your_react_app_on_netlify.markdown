---
layout: post
title:      "Deploying Your React APP on Netlify"
date:       2021-03-12 12:39:13 -0500
permalink:  deploying_your_react_app_on_netlify
---


You have built out your website, pushed it to GIthub and now you are ready to deploy. After doing some research and find that Netlify is the easiest and best way to deploy your site. Here are the steps to do so and a quick fix on a possible issue you may face.

Step 1: Create an account

Step 2: "Create a new site"

Step 3: Link your Github

Step 4: Pick your repository and "Deploy site" (You will see that it did not deploy)
(Error: npm ERR! code ELIFECYCLE)

Step 5: In your terminal run "npm run build"

Step 6: Go to deploy settings, navigate to "Build Command" and type in "CI= " before "npm run build"

Step 7: Go to Deploys tab, navigate to "Trigger deploy" and click "Deploy site"

Congratulations, your site is now up and running. Feel free to edit the domain name.





