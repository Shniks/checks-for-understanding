## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

#### 1. What is the entry at the command line to create a new rails app?

```ruby
rails new app_name -T -d="postgresql" --skip-Turbolinks --skip-spring
```

#### 2. What do Models generally inherit from in rails?

  - They inherit from ApplicationRecord  

#### 3. What do Controllers generally inherit from in a rails project?

  - ApplicationController  

#### 4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

```ruby
resources :horses, only: [:show]
```

#### 5. What rake task is useful when looking at routes, and what information does it give you?

```ruby
rake routes
```

  - It tells us the prefix, verb, uri and controller#action  

#### 6. What is an example of a route helper? When would you use them?

  - new_horse_path or horses_path  
  - Would use them if we don't want to know the full url  

#### 7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

  - Unsure what the question is asking  

#### 8. What are strong params and why are they necessary?

  - They are used for security and privacy and only pass the params we want to pass  

#### 9. What role does `form_for` play in helping us create our forms?

  - It helps to setup the form with the labels and text fields etc.  

#### 10. How does `form_for` know where to submit the user's input?

  - We pass the argument when initiating the form_for (i.e. @company or @idea)  

#### 11. Create a form using a `form_for` helper to create a new `Horse`.

```
<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.submit %>
<% end %>
```

#### 12. Why do we want to validate our models?

  - Want to make sure that clean data is being passed into our database tables  

#### 13. What are the steps of the DNS lookup?

  - Query, root servers, DNS

### Review Questions  

#### 14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

```
horse.move.prance
```

#### 15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  

```
furniture[:purchased]
furniture[:table][:height]
```

#### 16. What is inheritance?

  - Acquiring state and behavior from another class (usually a superclass)  

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week
