1. How do we make flash messages display on a page?

We first define a flash message in a controller method like so: `flash[:success] = "You have logged in!"` After that you iterate over the flash hash in your application.css so that it will display on all pages.

2. Where is cart information/temporary information usually stored?

In the sessions hash. This is an advanced cookie.

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?

Storing the cart in our database would lead to many useless records for people who discard their cart.

4. What is the purpose of the asset pipeline?

The asset pipeline minifies and compresses our assets into web servable files.

5. Why do we precompile our assets?

We precompile so that we can use other markup languages like SASS or HAML. Precompiling also speeds up performance.

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

The first tag is a link helper for the html <style> tag. This imports all of our custom styling. The second tag imports all of our javascript. The third tag is a url helper for <img src=""> that displays an image.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

Known bugs, workarounds, installation, features, how to contribute. The benefits are that your readme is essentially an "Elevator Pitch" for your application. A good README will get more users to download.

8. What are the top four accessibility issues that we as developers should be aware of?

Blindness, Colorblindness, Deafness, Mobility

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

It is a callback. A before_save is used to validate/concatenate records at the model level.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```

`scope :user -> {where(active:true)}`

11. What is the difference between a scope and a class method?

Scopes are essentially translated into class methods internally (`def self.something`).  Typically you use scopes for very small pieces of logic.
