# Ruby

## Setup Environment

Install `rbenv`

  brew update
  brew install rbenv ruby-build
  echo 'eval "$(rbenv init -)"' >> ~/.zshrc

Now we need to use rbenv (ruby environment) to set the ruby version. Enter this line from your project root folder:

`rbenv local 2.1.6`

## Successful completion

The ruby version on the workspace should be set to the latest ruby (version 2.1.6 as of this writing). They should be ready to create the new rails application in the project folder.

## Resources

* [rbenv](https://github.com/sstephenson/rbenv)
* [Comparison of RVM and rbenv](http://jonathan-jackson.net/rvm-and-rbenv)
* [Using rbenv to Manage Rubies and Gems](http://robots.thoughtbot.com/using-rbenv-to-manage-rubies-and-gems)