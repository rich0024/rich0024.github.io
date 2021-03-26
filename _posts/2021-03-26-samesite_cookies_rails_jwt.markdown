---
layout: post
title:      "Samesite Cookies Rails JWT"
date:       2021-03-26 20:05:14 +0000
permalink:  samesite_cookies_rails_jwt
---


With the chrome browser, unless specified, cookies are treated as "lax"; this means that cookies will be allowed if they are from the same site. However, for those who use React as their frontend and Rails as their backend, this causes an issue as the backend server operates at a different domain. Thus, chrome will not allow cookies to come from the backend server to the operational frontend. Thus, one must explicitly state that the samesite cookie is set to 'none'. This will allow the cookie to be sent to a site with a different domain. 

The code will look similar to the following:
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
Focus on the explicit 'SameSite=None'
