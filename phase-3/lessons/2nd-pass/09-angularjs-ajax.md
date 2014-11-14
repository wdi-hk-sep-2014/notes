# AngularJS $http

We are now able to link up between HTML & JavaScript, but both are on frontend. We want to link the data to our backend using Ajax. AngularJS provides Ajax using `$http`.

## Objective

To use `$http` to talk to server side.

## Steps

1) Add `$http` to the CoffeeScript

Just like the $scope, it allows the use of the variables, both provided by AngularJS library.

```
app.controller("TimetableCtrl", ["$scope", "$http", ($scope, $http) ->
```

2) Add the `Save` button to the page, this would send the data to server for processing

```html
<div class="col-md-2 col-md-offset-5 btn btn-success" ng-click="submitCount()">Save</div>
```

3) Define a new function `submitCount()` in CoffeeScript

```
  $scope.submitCount = ->
    jsonObj = {"data": $scope.weeks}
    $http.post('/api/lunches/submit', jsonObj)
      .success (data) ->
        console.log data
      .error (data) ->
        console.log data
```

4) Setup corresponding routes in `routes.rb`

```
    resources :lunches, only: [:index, :show, :create] do
      post  'submit'  , on: :collection
      get   'data'    , on: :collection
    end
```

## Successful Completion

- You should be able to send a POST request
- You should be able to get a response

## Reference Links

- [$http](https://docs.angularjs.org/api/ng/service/$http#post)
