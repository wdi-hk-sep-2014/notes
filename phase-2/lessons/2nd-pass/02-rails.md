# Rails

Create the new Rails application

## Procedure

We're going to create a blank Rails application now. We'll use the following command:

`rails new . -BGT`

Here's what all this means:

1. `rails` calls the rails executable; everything we pass after that is telling the rails application what we want it to do
2. `new` tells the rails executable that we want to create a new rails application
3. `.` tells the rails "new" script to create the application in the current folder, using the name of the folder as the name of the application
4. `-` is used to introduce options (flags) that customize the creation process
5. `B` tells the rails executable not to run bundler automatically (more on this anon -- we'll run it manually)
6. `G` tells the rails executable not to create its own .gitignore file (we're using GitHub's version)
7. `T` tells the rails executable not to include the testing framework (we'll add our own later)
8. `O` tells the rails executable not to include ActiveRecord (Leave it, we'll be using ActiveRecord)

You can see all the options for `rails new` by running `rails new -h`.

Now we have a basic rails application. But before we can run it, we have to install our dependencies. That's where bundler comes in.

## Successful completion

The team should have a blank Rails application in their project's root folder:

* Without having run bundler
* Using the GitHub supplied .gitignore file
* Without a testing framework

# Resources

- creator of rails: http://en.wikipedia.org/wiki/David_Heinemeier_Hansson
- [Rails Gem URL Shortener](https://github.com/jpmcgrath/shortener)
- [Getting Started guide](http://guides.rubyonrails.org/getting_started.html)
- [Ruby on Rails Tutorial Book](http://www.railstutorial.org/book)
- [Learn Ruby The Hard Way](http://ruby.learncodethehardway.org/book/)
- [Poignant Guide](http://mislav.uniqpath.com/poignant-guide/)
- [Ruby on Rails Guides](http://guides.rubyonrails.org/)
- [API Ruby on Rails](http://api.rubyonrails.org/)