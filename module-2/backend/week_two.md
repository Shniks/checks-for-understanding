## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

#### 1 . At a high level, what is ActiveRecord? What does it do/allow you to do?  

  - ActiveRecord is the 'M' in MVC and is a library for working with Relational Databases. It allows us to query our database and is responsible for the logic.  

#### 2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?  

  - We have access to these methods the concept of inheritance. The 'Team' class inherits these methods from ActiveRecord. Some of the methods are `all`, `find`, `where`, `find_each`, `order`, `select`

#### 3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?  

  - `team = Team.find(4)`  
  - `Owner.find_by(team: team)`

#### 4. Assume that you added a line to your `Team` class as follows:  

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?  

  - `Team.find(4).owner`

#### 5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.  

  - Students: (ID, name)  
  - Teachers: (ID, name)  
  - Student_Teachers: (id, Student_ID, Teacher_ID)  

#### 6. Define foreign key, primary key, and schema.  

  - Primary Key: is used to uniquely identify each row in the table  
  - Foreign Key: refers to the primary key in the other table and is used to link an external table with the table  
  - Schema: shows the skeletal structure of the database  

#### 7. Describe the relationship between a foreign key on one table and a primary key on another table.  

  - The foreign key refers to the primary key in the other table  

#### 8. What are the parts of an HTTP response?  

  - Status, headers and body  

### Optional Questions

#### 1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.  

  - find: returns data based on the id  
  - count: returns the number of data items
  - order: orders the records (can be descending or ascending)
  - sum: sums the data based on a criteria
  - limit and offset: returns a maximum number of records (the limit number) starting from a specified record number (the offset)  

#### 2. Name your three favorite ActiveRecord rake tasks and describe what they do.  

  - rake db:drop = drops the database  
  - rake db:reset = drops, creates, migrates and seeds the database  
  - rake db:test:prepare = essentially clones the database to conform to the schema to take into account any pending migrations

#### 3. What two columns does `t.timestamps null: false` create in our database?

  - `created_at` and `updated_at`

#### 4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?  

  - A school has_many teachers and a teacher belongs_to a school  

#### 5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?  

  - Schools: (ID, name)  
  - Teachers: (ID, name, School_ID)  

#### 6. Give an example of when you might want to store information besides ids on a join table.  

#### 7. Describe and diagram the relationship between patients and doctors.  

  - Doctors: (ID, Name)  
  - Patients: (ID, Name)  
  - Patient_Doctors: (ID, Patient_ID, Doctor_ID)  

#### 8. Describe and diagram the relationship between museums and original_paintings.  

  - A museum has many original paintings and the original paintings belong to a museum  

  - Museum: (ID, name)
  - Original Paintings: (ID, name, Museum_ID)  

#### 9. What could you see in your code that would make you think you might want to create a partial?

- Information that is being repeated  

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
