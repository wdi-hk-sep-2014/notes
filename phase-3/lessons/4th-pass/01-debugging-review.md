# Network Request Debugging Exercise

## Setup

Make a clone of the [PepperLunch upstream repository](https://github.com/wdi-hk-sep-2014/PepperLunchClone) in a folder called `PepperLunchDebugging`:

```sh
git clone git@github.com:wdi-hk-sep-2014/PepperLunchClone.git PepperLunchDebugging
```

Checkout the `broken_1` branch:

```sh
git checkout broken_1
```

Make sure Postgres is running, then set up your database:

```sh
rake db:create
rake db:migrate
```

Run your rails server, visit the site in your browser.

## Problems

1. When I load the page, it seems like the lunch count is missing. Fix it!

2. When I try and save my lunches, it doesn't seem to work, since when I refresh the page, my checked lunches aren't there. Fix it!

## Debugging techniques questions

1. How do you check in the browser what data has come back from an AJAX GET request?
2. How do you stop the execution of JavaScript at a particular line so you can step inside the code and debug it? (at least 2 ways)
3. How do you stop the execution of your Rails server code at a particular line so you can step inside the code and debug it? (at least 2 ways)
4. How do you check what data was sent to the server in an AJAX POST request, either in the browser or on the Rails server? (at least 1 way in the browser, at least 3 ways in the server)

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
answers are below  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
don't cheat  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
no really, I see you trying to cheat  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
what would your mother say  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## Debugging techniques answers

1. Use the Network tab of the Developer Tools. Click the request you are interested in, then view the response in either the "Preview" or "Response" tab.
2. At least two ways:
  * Add a line in your JavaScript code that says `debugger`.
  * In the Sources tab of the Developer Tools, navigate to the file using the directory viewer on the left (find JavaScript files in the assets directory), then click the line number that you want to stop code execution. This sets a _breakpoint_ on that line -- a point in the code where you want to break the flow of execution so you can see what's happening.
3. At least two ways:
  * Add a line in your Rails code that says `binding.pry`. This will stop the code **in the terminal window where your server is running**, and give you an interactive Ruby prompt (`pry`) where you can inspect the state of the code. *(Note: this requires including the `pry` and `pry-rails` gems in your Gemfile)*
  * Add a line in your Rails code that says `raise`. This will stop the code **in the browser where you are accessing your app**, and give you a similar interactive Ruby prompt, plus information about the parameters in the request and the current values of the variables. *(Note: this requires including the `better_errors` and `binding_of_caller` gems in your Gemfile)*
4. At least one way on the client, three ways on the server:
  * *Browser:* Use the Network tab of the Developer Tools as in #1, but this time check the "Headers" tab and look for the "Request Payload" section.
Three ways on the server:
  * *Server:* Check the terminal where your Rails server is running. For every request your server handles, it will show a line like `Started POST "/api/lunches/submit.json" for...`. Under that line will be other information about the request, including a line showing the request parameters like `Parameters: {"lunch"=>{...}}`
  * *Server:* Use `binding.pry` as in #2
  * *Server:* Use `raise` as in #2
