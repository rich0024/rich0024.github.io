---
layout: post
title:      "Samesite Cookies Rails JWT 2"
date:       2021-03-30 23:33:38 +0000
permalink:  samesite_cookies_rails_jwt_2
---


I was wrong! In my previous blog I discussed how to change same site cookie attributes, but my syntax was incorrect. This is a simple mistake that went over my head and caused many issues with my code. Previously, the code I used was written in Javascript inside a rails document. This is such a silly mistake, but with flipping between the languages, it was a mistake bound to occur and learn from.

Here is the mistaken code:
```
    def create
        user = User.new(user_params)
        if user.save
        created_jwt = encode_token({id: user.id})
        cookies.signed[:jwt] = {value: created_jwt, httponly: true, expires: 1.hour.from_now, SameSite=None}
        render json: user
        else
            render json: {error: 'Error creating user'}
        end
    end
```

On the 5th line there is camel cased writing, which is not the proper convention for Ruby. After running this code, I received errors that i needed to shut off my cors. After constantly playing around with the cors, I realized that everything in my cors was correct so there must be another issue. Thus, I traced back my steps and found this glaring mistake. After using the proper ruby convention, everything is up and running.

Here is the proper code:
```
    def create
        user = User.new(user_params)
        if user.save
        created_jwt = encode_token({id: user.id})
        cookies.signed[:jwt] = {value: created_jwt, httponly: true, expires: 1.hour.from_now, same_site: none, secure: true}
        render json: user
        else
            render json: {error: 'Error creating user'}
        end
    end
```
