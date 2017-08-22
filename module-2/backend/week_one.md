## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

* GET - client requests information

* PUT - client sends information

* POST - works in conjunction with PUT

* PATCH - updates information

* DELETE - destroys information

2. What is Sinatra?

A lightweight web framework written in Ruby based on Rack

4. What is MVC?

MVC stands for Model, View, Controller, a systematic approach to object oriented web design

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

In order to prepare for all the things Rails offers us, and that web conventions are normally the same across all frameworks

6. What types of variables are accessible in our view templates without explicitly passing them?

Params

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

@name = "Mr. Ed"

9. What's the purpose of ERB?

It's essentially html markdown in which ruby variables can be passed

10. Why do I need a development AND test database?

The test database is for spec tests, it cleans itself 

11. What's responsive design?

Resizes itself for different screen sizes

12. What is CRUD and why is it important?

Create, Read, Update, Delete, it is the foundation for most database based applications.

13. What does HTTP stand for? 

HyperText Transfer Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

<%= and <%. The former is for a single line, the latter a block.

15. What's an ORM?

Object Relational Mapping, turning sets of data into code objects

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?

ActiveRecord

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

* /restaraunts - GET
* /restaraunt/:id - GET
* /restaraunt/:id/edit - PATCH
* /restaraunts/new - PUTS & POST
* /restaraunts/:id/delete - DELETE

18. What's a migration?

A modification to the database

19. When you create a migration, does it automatically modify your database?

No, one must run `rake db:migrate`

20. How does a model relate to a database?

A model is the singular noun of a table

21. What's the difference between agile workflow and waterfall method?

Agile is a milestone approach, waterfall is all at once.

22. What is the difference between `#new` and `#create`?

With #new you must also call #save, #create doe both
