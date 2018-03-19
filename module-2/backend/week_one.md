## Week One - Module 2 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

#### 1. List the five common HTTP verbs and what the purpose is of each verb.
  - GET: is used to read a resource.
  - POST: is used to create a resource.
  - PUT: is used to update or replace a resource.
  - PATCH: is used to update or modify a resource.
  - DELETE: is used to delete a resource.
#### 2. What is Sinatra?
  - is a framework that enable web interaction.
#### 4. What is MVC?
  - Model: is the logic and allows interaction with the database.
  - View: is what is displayed on a user's browser.
  - Controller: is a liaison between the controller and the model. It collects the information from the model and then displays it in the browser based on the specified path.
#### 5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  - To bring consistency across the web.
#### 6. What types of variables are accessible in our view templates without explicitly passing them?
  - Any instance variable
#### 7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  - Answer

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

#### 8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
    name = "Mr. Ed"
    erb :index, locals: {name: name}
  end
  ```
#### 9. What's the purpose of ERB?
  - To display the information from the controller in a web browser.
#### 10. Why do I need a development AND test database?
  - Unsure. Maybe to keep the test database separate from the development database to ensure integrity?
#### 11. What is CRUD and why is it important?
  - Create, Read, Update and Destroy.
#### 12. What does HTTP stand for?
  - Hyper Text Transfer Protocol.
#### 13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  - <% %> : Doesn't print the information.
  - <%= %> : Prints the information.
#### 14. What's an ORM?
  - Object Relational Mapper: can create ruby object from rows, where each row represents an instance of a class with the columns as attributes.
#### 15. What's the most commonly used ORM in ruby (Sinatra & Rails):
  - ActiveRecord.
#### 16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  - GET '/restaurants': shows a page with all the restaurants.
  - GET '/restaurants/:id': shows a particular restaurant based on id.
  - GET '/restaurants/new': Go to a page where can fill details to create a new restaurant.
  - POST '/restaurants': creates the new restaurant.
  - GET '/restaurants/:id/edit': Go to a page to where can fill details to edit a restaurant.
  - PUT '/restaurants/:id': Updates the restaurant.
  - DELETE 'restaurants/:id': Deletes the restaurant from the database.
#### 17. What's a migration?
  - We use migrations to create instructions when we want to create or update a database (e.g. what the attributes will be).
#### 18. When you create a migration, does it automatically modify your database?
  - No, it does not. We have to run rake db:migrate to modify it.
#### 19. How does a model relate to a database?
  - We use the model to fetch the data from the DB and then pass it on to the controller (which can then send it to the view).
#### 20. What is the difference between `#new` and `#create`?
  - new does not save the instance (we have to still use save after using new), while create will create and save the instance.

### Review Questions:  
#### 21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  -  ```ruby
      CSV.foreach(/"films.csv", :headers => true, header_converters: symbol) do |data|
          film = Film.create(title: data[:title], description: data[:description])
     ```
      NB: the id will be created automatically.
#### 22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?

  - same as inserting into a hash, viz. activities[:hiking][:supplies].push("granola bar")
#### 23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  - Abstraction: showing only the essential features and hiding the details.
  - Encapsulation: containing the state and behavior in a class.
  - Inheritance: is used to inherit methods etc. from another class or module. It's to reuse code that has already been written.
  - Polymorphism: I know this exists, but not sure of the definition.
### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
  - I had to refer to my notes for the definition of Sinatra and ORM. Other than that, I am not sure if some of my answers completely answer the question.

Choose One:
* I feel comfortable with the content presented this week
  - I still need to practice MVC more to get more comfortable with it. I think the little shop project is good as it made us do a bunch of these methods. But I still need more practice to really get familiar with the concept and have it be second nature.
