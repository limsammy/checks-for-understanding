## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?

A cookie is a way to make HTTP have state. It is something the server gives the client to save locally.

* What’s the difference between a session and a cookie?

A session is a more sophisticated form of cookie. It is encrypted and has somem other friendly Rails features.

* What’s a flash and when do you want to use flashes?

Flashes are popup messages you can set up to show after a certain action, and can be used with conditionals (Failure/success messages)

* Why do people say “HTTP is stateless”?

Every time the client makes a request the history has been cleared and there is no prior history associated with the request.

* What’s authentication? Explain.

Authentication is giving the user a secret token after who they say they are is verified.

* What’s the difference between authentication and authorization?

Authorization is the concept of limiting access for specific roles.

* What’s a before filter?

A before_filter is a helper that executes a method before anything else in that controller/model is instantiated.

* How do we keep track of a user once they’ve logged in?

By storing the user's id in a session.

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

We namespace resources in order to alter the path. Nesting resources is more when you want to associate a child object with a parent.

* At a high level, what tools can you use to implement authorization? How would you use them?

BCrypt, Sessions, defining routes. You can define new routes for sessions to be created, encrypting everything with BCrypt before it enters the databasea.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

An enum essentially translates an integer to a string.

* What are some strategies you can use to keep your views DRY?

Always breaking logic out to helpers.
