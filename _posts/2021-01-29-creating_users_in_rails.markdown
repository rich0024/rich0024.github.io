---
layout: post
title:      "Creating Users in Rails"
date:       2021-01-29 18:43:30 +0000
permalink:  creating_users_in_rails
---


First, run 'rails generate resource User' in order to create a user migration, user model and a user controller.

Next, check the gemfile and see if 'bcrypt' is enabled. Bycrypt is a gem that encrypts a user's password upon creation and stores the encrypted password. This acts as a line of security so even the app creator does not have access to one's password. We will revisit this later on.

```
gem 'bcrypt', '~> 3.1.7'
```

After 'bcrypt' head into the db --> migrations --> [user migration] 
Here, you can add in properties of a user. Typically, a user will ofter have a username, email and password. However, associations and other properties can be added here as well. Here is an example from a recipe app I created:
```
class CreateUsers < ActiveRecord::Migration[6.0]
  def change
    create_table :users do |t|
      t.string :username
      t.string :email
      t.string :password_digest

      t.timestamps
    end
  end
end
```
(note that 'password_digest' is here as part of the bcrypt gem)
Once, completed, run 'rails db migrate'

Next go into the user model file. Here you can set user specific methods, associations and validations. 
Example:
```
class User < ApplicationRecord
    has_secure_password

    has_many :my_recipes
    has_many :recipes, through: :my_recipes
end
```
'has_secure_password' is also part of the bcrypt gem.

Finally, open the user controller. Here, there will be some variation depending on the front end. The example I will show is for a react based app. The main methods to pay attention to are the create and show methods.
```
class UsersController < ApplicationController
    before_action :authenticate_user, only: [:show]

    def index
        users = User.all
        if users
            render json: users
        else 
            render json: {
                error: 'no users found'
            }, status: 500
        end
    end

    def show
        user = User.find(params[:id])
        if user
            render json: user.recipes
        else
            render json: {
                status: 500,
                errors: ['no users found']
            }
        end
    end

    def create
        user = User.new(user_params)
        if user.save
        created_jwt = encode_token({id: user.id})
        cookies.signed[:jwt] = {value: created_jwt, httponly: true, expires: 1.hour.from_now}
        render json: user
        else
            render json: {error: 'Error creating user'}
        end
    end

    private

    def user_params
        params.require(:user).permit(:username, :email, :password)
    end
end
```

