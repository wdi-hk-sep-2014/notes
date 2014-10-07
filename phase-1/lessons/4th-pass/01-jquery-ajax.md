## jQuery AJAX

- Asynchronous
- HTTP methods (GET / POST / PUT / DELETE)

```
response = $.ajax(
  "http://www.omdbapi.com/?s=Matrix"
  dataType: "json"
)

response.done (data) ->
  movies = data.Search
  for movie in movies
    li = "<li><a href='#' data-imdbid='#{movie.imdbID}'>#{movie.Title}</a></li>"
    $('.movies').append(li)
  $('a').click (e) ->
    imdbID = $(@).data('imdbid')

    $.ajax(
      "http://www.omdbapi.com/?i=#{imdbID}&plot=full"
      dataType: "json"
    ).done (data) ->
```

## JSON

- JavaScript Object Notation

```
{
    staff: {
        id: 1,
        name: 'Harry',
        salary_rate: 'poor'
    }
}
```

# Code Challenge

Build a API for Open Movie Database (OMDB)

```
<script type="text/javascript">

// IMDb ID to Search
var imdbId = "tt1285016";

// Send Request
var http = new ActiveXObject("Microsoft.XMLHTTP");
http.open("GET", "http://www.omdbapi.com/?i=" + imdbId, false);
http.send(null);

// Response to JSON
var omdbData = http.responseText;
var omdbJSON = eval("(" + omdbData + ")");

// Returns Movie Title
alert(omdbJSON.Title);

</script>
```

## Resources

- http://www.omdbapi.com/
- http://gearside.com/public-json-feeds/
- http://www.jsontest.com/
- [AJAX Programming](http://en.wikipedia.org/wiki/Ajax_(programming))
- [9 Cool Public JSON Feeds](http://gearside.com/public-json-feeds/)
- [OMDB API](http://compare-movies.bitballoon.com/)

## Very Old Website
