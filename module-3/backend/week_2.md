## Week Two - Module 3

Some of these questions are from this week, some are from previous weeks, and some are new concepts. Try answering without research first. If you are not sure, take a guess but acknowledge that it's a guess (faking an answer in an interview without acknowledging it as a guess is a bad idea). Follow up with the necessary research to understand these concepts. These tend to be common themes during the job hunt and are worth having a solid understanding of.

1. What's OAuth? 

OAuth is an external service that moves authentication to a third party.

2. What are some advantages/disadvantages of implementing OAuth?

Advantages are that you don't have to worry about implementing authorization services like storing passwords, tokens, etc. Disadvantages include not having an account for the service provider.

3. What are the four pillars of object oriented design? How do they apply when creating:
  * services?
  
  Abstraction, encapsulation, inheritance, and polymorphism. Services are specific implementations of polymorphism concepts, abstraction, and inheritance. We break out the unique identity of the service by abstracting it to it's own class with a set of attributes unique to itself.
  
  * PORO's with the data received from an API?
  
  It takes in the elements of all 4 pillars. Code complexity is broken down through abstraction, and the POROs belong to a specific class. However they are flexible as well.
  
4. What do we use VCR for? Why is it a good idea to use this tool?

We use VCR to record HTTP responses for 'playback'. This is useful when testing API responses, as we can test our methods in isolation.

5. What does HTTP stand for?

Hyper-Text Transfer Protocol

6. What class does `ApplicationController` inherit from when creating a Rails project with the `--api` flag? What about without the `--api` flag?
  * What is `protects_from_forgery`?
  
  ApplicationController inherits from ActionController::API versus ActionController::Base. This leaves out most browser-only ActionController features. Protects_from_forgery protects against CSRF.
  
  * What do you need to do differently for your API to accept non-GET requests if you did not use the --api flag?
  
  You need to inherit from ActionController::API.
  
7. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)
   
   AR: rails g model first_name last_name email age:integer
   SQL: CREATE_TABLE users (
     first_name string,
     last_name string,
     email string,
     age integer)
   
8. What does `inject` do? How should you use it?

Inject combines all elements of a hash by applying a binary operation. 

#### Self Assessment  
Rate yourself on the following scale.  
4 I know and understand all these concepts and did not have to look anything up  
**3 I know and understand most of these concepts but had to look something up**
2 I am uncertain about some of these concepts and had to look some things up ^^  
1 I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up.
