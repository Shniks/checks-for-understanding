### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions

#### 1. How do we make flash messages display on a page?

```
<% flash.each do |type, message| %>
<%= content_tag :div, sanitize(message), class: name %>
<% end %>
```

#### 2. Where is cart information/temporary information usually stored?

  - In a session

#### 3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?

  - Might not want to store a cart in a DB as it is temporary information. We would want to persist that information as http is stateless and we want to be able to see what is in a cart during different requests. A session allows http to maintain state and remember the information in the cart.

#### 4. What is the purpose of the asset pipeline?

  - To keep all the javascript, css and image assets in one place to minimize the number of http requests. It is implemented by the sprockets-rails gem.

#### 5. Why do we precompile our assets?

  - We might need to precompile assets if we need to debug the production environment and want to see the specific version that will be used in production. Heroku precompiles the assets for us automatically, so only try and manually precompile if Heroku is having issues precompiling.

#### 6. What do each of the following tags do?

```
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

  - link to the stylesheet manifest, javascript manifest and link to an image called rails.png

#### 7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

  - A good readme describes the purpose of the project, provides the steps for installation and running the project. It provides samples of the code to show how we can use the project along with snapshots of the code.

#### 8. What are the top four accessibility issues that we as developers should be aware of?

  - Visual, mobility, alternative browsers, older devices, cognitive

#### 9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

  - It is a callback used in models

#### 10. Given the following object, how would we create a scope for all users who are active?


```ruby
User.create(name: "Happy", active: true)
```

  - scope :active, {where(active: true)}

#### 11. What is the difference between a scope and a class method?

  - scope returns a subset of objects for the class while a class method finds more information.


### Review Questions:  

#### 12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  

    ```ruby
    - given[:cart]["48"] = 4
    ```

  12b. How would you increase the quantity of item 29?  

    ```ruby
    - given[:cart]["29"] += 5 (or whatever number it is to increase by)
    ```

  12c. How would you find out how many items your user is thinking about purchasing?   

    ```ruby
    - given[:cart].values.sum
    ```


#### 13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  

  - Polymorphism allows us to create methods of the same name. It thus allows us to use the same method with different results when used on different objects. Duck-typing means if it looks like a duck and walks like a duck, it is a duck.

#### 14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  

  - can use gsub


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
