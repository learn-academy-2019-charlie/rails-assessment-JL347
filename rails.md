# Rails Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

### 1. What are some advantages of using Ruby on Rails?

- it's a stream-lined way to create a full web app quickly.
- the syntax is a little bit easier to pick up
- it's suitable for a lot of different industries

### 2. How does Ruby on Rails use the Model View Controller (MVC) framework?

- it uses by sending requests from the router to a database. A request will pass through models, views and controllers to the database and then back to the router.

### 3. Using the information given, complete the steps for creating a new view in a rails app by filling in the blanks:

  1. Create a route: 
  
  code: 
  ```
  get '/about' => 'statics#about' 
  ```
  file: config/routes
  
  2. Create the ____controller_______
  
  code: 
  ```
  class ______StaticsController______ < ApplicationController
  
  def about 
    _________render 'statics.html.erb'______________
  end
  ```
  
  file: _________static_controller.rb____________
  
  3. Create the View
  
  code: 
  
  ```
  <div>This is the About page!</div>
  ```
  
  file: _________ views/static/statics.html.erb ____________
  
  
### 4. Look at these sets of Rails routes, they are an example of which principle/term that we touched on briefly in class? Find the term, and explain why it is important.

```
/users/       method="GET"     # :controller => 'users', :action => 'index'
/users/1      method="GET"     # :controller => 'users', :action => 'show'
/users/new    method="GET"     # :controller => 'users', :action => 'new'
/users/       method="POST"    # :controller => 'users', :action => 'create'
/users/1/edit method="GET"     # :controller => 'users', :action => 'edit'
/users/1      method="PUT"     # :controller => 'users', :action => 'update'
/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy'
```

- these files are created when we generate resources. they are used to follow the CRUD guidelines and are important because it allows you to interact with the database.

### 5. What is the public folder used for in Rails?

- the public folder is used to hold all of the stylings for certain errors that may occur. Such as the 404 error, etc.

### 6. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

-  get '/game/guess' => 'main#game' 

### 7. What are cookies for? How do they work? What is the difference between a session and a cookie?

- Cookies are key-value data pairs that are stored in the user’s browser until they reach their specified expiration date. Cookies allow you to keep track of your user from request to the other. A session is simply the length of time between requests.

### 8. In an html form, what does the "action" attribute tell you about the form?  How do you designate the HTTP verb for the form?

- the action attribute will say whether the form is a GET or a POST. you have present it in all caps

### 9. Why would you use an instance variable in a rails controller?

- in order to use that variable elsewhere, you would make an instance variable. Ex: @name

### 10. Name two rails generator commands and what files they create:

- rails g model will create a brand new model
- rails g migration will enable you to add a new column to a table. Ex: rails g migration add_to_fieldname_to_tablename fieldname:string

### 11. Rails has a great community and lots of free tutorials to help you learn. Here is a list of some tutorials to choose from, choose one, do it, and then report back here at least one thing you learned. You can also use a different resource if you find one that you like better. 

- https://www.tutorialspoint.com/ruby-on-rails/index.htm
- http://railsforzombies.org
- http://guides.rubyonrails.org/getting_started.html


 - I read about Layouts during my research. Layouts reside in the views section of your file and define the common look of your final output. Essentially you create a template and then let the controller know it exists and implement it.