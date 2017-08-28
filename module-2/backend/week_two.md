## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

ActiveRecord is one of the most common out of several ORMs used with Ruby on Rails. It allows you to interact with databases much more easily through the Ruby and Rails framework.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

`Team.all`, `Team.all.first.create`, `.delete`, `.find_by` `.update`; We have access to these due to the fact that our Team model inherits the library of ActiveRecord/Base. 

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

````t = Team.find(4).name```` 

```Owner.find(t)```


4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

`Team.find(4).owner`

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Teacher has many Students, a Student belongs to a Teacher

```table students
|      id    |
|     name   |

table teachers
|     id     |
|    name    |
| student_id |```

6. Define foreign key, primary key, and schema.

A primary key is the `id` of a table. It is the key that is inserted to an associated table. The key referenced in the associated table is the `foreign key`. The schema is a blueprint of the database and all of your migrations.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

A foreign key is the has_many part of an association, while a primary key is the id being inserted as the foreign key.

8. What are the parts of an HTTP response?

status, header, body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
