# jQuery

## Objective

- To understand the use of local and CDN jQuery library
- To make use of jQuery CSS Selector
- To dynamically change page style using jQuery

## Use External jQuery

Sometimes, you would need to use external link due to: 

1. You don't want to duplicate hosting the jQuery library
2. You don't want to manage the library version yourself
3. You don't want your users to use up your own bandwidth

However, other time you are necessary to host it in your own server:

1. You have a disconnected, private web environment
2. You are in China, with the Great Firewall environment blocking the traffic
3. Your Internet connection is really bad

To use external jQuery, we will find the link from CDN (e.g. Google Hosted Libraries)

1. Search `jquery cdn google`
2. Get into [Google Hosted Libraries - Developer's Guide](https://developers.google.com/speed/libraries/devguide?hl=zh-tw)
3. Look up to `jQuery`
4. Copy the snippet `<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>`
5. Paste or replace the link to jQuery in the HTML file.

```
Remarks:

The external link does not have http or https, it will depend on the environment you are visiting. (ie. http or https) Be sure that you are not using file:// to get the jQuery library.
```

## Changing Background (JavaScript)

```
$(document).ready(function() {

  function randomColor() {
    return '#' + Math.random().toString(16).slice(2, 8);
  }

  $('#bgBtn').on("click", function() {
    console.log("Hello Harry!");

    $('.navbar').css('background', randomColor());
  });

});
```

## Prevent Default event

```
event.preventDefault()
```

## Successful Completion

- You are able to update the background color randomly by clicking a button.

## Reference Links

- [jQuery .on()](http://api.jquery.com/on/)
