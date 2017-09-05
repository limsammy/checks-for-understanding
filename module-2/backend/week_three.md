## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

rails new NAME -T --database=postgresql --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?

Rails' ApplicationRecord

3. What do Controllers generally inherit from in a rails project?

Rails' ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

resources :horse, only [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

rake routes, this gives you the action, path, and URL

6. What is an example of a route helper? When would you use them?

A route helper is something like `link_to` where you can pass it ActiveRecord objects.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

\_url is the URI pattern, whereas path is the actual path to the object/view

8. What are strong params and why are the necessary?

Strong params are calling params directly, not through your protected validation method. This is necessary when allowing the user to sort.

9. What role does `form_for` play in helping us create our forms?

`form_for` allows us to pass in a ruby object (or multiple objects) for easy form building using erb tags.

10. How does `form_for` know where to submit the user's input?

Through it's initialization, we pass it ruby object(s).

11. Create a form using a `form_for` helper to create a new `Horse`. 

```form_for @horse do |f|
    f.label :name
    f.text_field :name
    
    f.submit
 end```

12. Why do we want to validate our models?

So dangerous paramaters are not passed to our controller and database (prevents attacks like SQLi)
