## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

#### 1. What is a cookie?

  - A cookie is a piece of data stored on the user's computer by the user's browser.

#### 2. What’s the difference between a session and a cookie?

  - A cookie is stored on the user's computer while a session is on the server side.

#### 3. What’s a flash and when do you want to use flashes?

  - A flash message is a message displayed for a brief time for a controller action.

#### 4. Why do people say “HTTP is stateless”?

  - HTTP is stateless as the connection between the browser and server is lost once the session ends.

#### 5. What’s authentication? Explain.

  - Authentication is the process of verifying the user and who they are. Are they who they say they are?

#### 6. What’s the difference between authentication and authorization?

  - Authentication is to verify the identity of a user while authorization is the process to determine what permissions a user has.

#### 7. What’s a before filter?

  - A before filter run before any action in the controller.

#### 8. How do we keep track of a user once they’ve logged in?

  - We keep track of the user via our session.

#### 9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

  - Namespacing is used to organize the controller for a resource and change the route that the user would visit.

#### 10. At a high level, what tools can you use to implement authorization? How would you use them?

  - Namespacing to organize the controllers
  - Using the before_action (e.g. before_action :require_admin) to put restrictions on who sees what.

#### 11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

  - Allows us to associate symbols to reference which will be stored in the db as an integer.

#### 12. What are some strategies you can use to keep your views DRY?

  - Partials


### Reviews Questions
#### 13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

  - Unsure about what the question is asking. I noticed that each of the elements in the array was also missing the closing curly bracket.

#### 14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

  - given.split('$').last.to_i


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
  - I am sort of in-between the two. I feel that I need to revise the content more as I have a little hard time articulating.
