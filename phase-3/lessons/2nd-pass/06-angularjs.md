# AngularJS

HTML is used for layout and structure, we need to use JavaScript or jQuery to modify the content dynamically. If the site becomes more complex, the management of JavaScript would be huge work. We thus want better ways.

## Objective

To start using AngularJS, try some examples, and turn our PepperLunch Tracker to a single page application.

Remarks: AngularJS can do most jQuery works, but they can work together as well, so we will keep jQuery in our project.

## Steps

1. Visit https://angularjs.org/, try the examples on the home page
2. Install angularjs thru Gemfile, by putting `gem 'angularjs-rails'`
3. `bundle install`
4. In `application.js`, and the line of `//= require angular` just before `//= require_tree .`
5. In `application.html.erb`, add `ng-app` to the `body` tag as an attribute
6. Copy the first example code from official site to our application
  - Copy the `<input type="text" ng-model="yourName" placeholder="Enter a name here">`
  - Copy the `<h1>Hello {{yourName}}!</h1>`
7. Refresh the page, the input field comes out, try it out!!

## Successful Completion

- You will be able to view your name after inputting to text field

## Reference Links

- [AngularJS](https://angularjs.org/)
- [AngularJS 2048](http://www.ng-newsletter.com/posts/building-2048-in-angularjs.html)
- [Angular Rails](http://angular-rails.com/)
