# Bootstrap Starter Template

Visit http://getbootstrap.com/getting-started/#examples-framework

Since we will be using Bootstrap for this project, we can borrow the template elements from the official site, and build our application on top of that. We will be using a mix of `Starter template` and `Grids`.

## Objective

To bootstrap our application with template.

## Steps

1. Visit `Starter template`, inspect the navigation bar.
2. Copy the source code to our `application.html.erb`
3. Modify the text of title, links
4. Use `link_to` helper function for the hyperlink
5. Do the same to the div area of class container
6. Then, visit `Grids`, do the same to the Three equal columns
7. Copy the corresponding CSS, by looking at the Styles pane on the right
8. Modify `col-md-4` to `col-md-2`, and prepare six columns for a row

```html
  <nav class="navbar navbar-inverse navbar-fixed-top" role="navigation">
    <div class="container">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand" href="#">Project name</a>
      </div>
      <div id="navbar" class="collapse navbar-collapse">
        <ul class="nav navbar-nav">
          <li class="active"><a href="#">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div><!--/.nav-collapse -->
    </div>
  </nav>
```

## Successful Completion

- You should have a page with the navigation bar
- You should have a header with welcome message
- You should have a board of 13 rows, with 6 columns in everyone
- There will be some basic CSS styles

## Reference Links

- [Starter template](http://getbootstrap.com/examples/starter-template/)
- [Grids template](http://getbootstrap.com/examples/grid/)

