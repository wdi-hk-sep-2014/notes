# Managing dependencies with bundler

The objective is for the team to learn a bit about dependency management in Rails.

## Procedure

All rails applications have dependencies on other applications. We need to tell rails which dependencies this rails application uses. There are many ways to do this, but the current best practice is to use a program called *bundler*.

We will need to first modify the `~/.gemrc` file with the following:

```
---
:update_sources: true
:sources:
- http://gems.rubyforge.org/
- http://gems.github.com
:benchmark: false
:bulk_threshold: 1000
:backtrace: false
:verbose: true
gem: --no-ri --no-rdoc
```

Bundler has to be installed before we can use it. We can install the latest version from our project root folder with the command:

`gem install bundler`

Once it is installed, we'll want to update our Gemfile, and then run it to install the dependencies. In the project root folder, you should find a file called *Gemfile* that the rails executable created. Open it and replace the contents with these:

    source 'https://rubygems.org'

    gem 'rails', '4.1.6'
    gem 'sqlite3'
    gem 'sass-rails', '~> 4.0.3'
    gem 'uglifier', '>= 1.3.0'
    gem 'coffee-rails', '~> 4.0.0'
    gem 'jquery-rails'
    gem 'jquery-ui-rails'
    gem 'spring',        group: :development

    group :development, :test do
      gem 'better_errors'
      gem 'binding_of_caller'
    end

What do these do?

1. `source` tells bundler where to find these gems
2. `rails` tells bundler to install version 4.1.1 of rails (required)
3. `activesupport` installs a lot of extra features we may want to use (optional: later we can decide which we'll actually use and "cherry pick" those so we aren't loading everything)
4. `require: 'active_support'` makes those extra features available everywhere in our application (optional: without this line we'd have to add them at the top of each file where they're used)
5. `uglifier` adds a JavaScript compressor that rails needs; we'll use this on every rails app
6. `jquery-rails` and `jquery-ui-rails` add the jQuery JavaScript library that rails uses; we'll probably use these on every rails app
7. `group` groups a few dependencies together and loads them *only when we're in the mode(s) specified*; in this instance, we are loading these dependencies only in the **development** and **test** mode, but not in the **production** mode
8. `better_errors` gives us a nice, in-browser error page that makes debugging easier
9. `binding_of_caller` gives us some advanced features for the better_errors gem

Now we can install these dependencies with the following command (in the project root folder):

`bundle install`

This will take a while. When your bundle is installed, we should be able to run the rails application:

`bundle exec rails server`

This will start up a Webrick server (included with rails) and will serve your new rails application at  [localhost:3000](http://localhost:3000/). Check it out.

We'll be adding more dependencies as we need them and then updating our bundle.

## Successful completion

Upon successful completion of this lesson, the team should have:

1. Installed the bundler gem
2. Updated their application's Gemfile to the one shown above (update as necessary)
3. Installed the dependencies
4. Checked to make sure that their application works by running the Webrick server

The should also have some idea what each line in the Gemfile does, even if they don't understand yet what the dependency itself does.

## Resources

* [Rails ActiveSupport Guide](http://guides.rubyonrails.org/active_support_core_extensions.html)
* [Uglifier](https://github.com/lautis/uglifier)
* [Better Errors](https://github.com/charliesome/better_errors)
* [binding_of_caller](https://github.com/banister/binding_of_caller)
* [Make --no-ri --no-doc by default](http://stackoverflow.com/questions/1381725/how-to-make-no-ri-no-rdoc-the-default-for-gem-install)