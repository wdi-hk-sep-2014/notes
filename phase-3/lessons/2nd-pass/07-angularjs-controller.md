# AngularJS (ng-controller)

AngularJS is positioned as Model-View-Whatever (MVW) framework, being the JavaScript variables as the model (storing the data), and HTML as the view.

It uses a decorator called Controller to represet the "whatever" part.

## Objective

To implment ng-controller, which will help to better scale an AngularJS app.

## Steps

1) Give a value to `ng-app` in `application.html.erb`, say `myApp`

```html
<body ng-app="myApp">
```

2) Define the module in CoffeeScript

```
App = angular.module("myApp", [])
```

3) Add `ng-controller` to the `html.erb` file

```
<div class="timetable" ng-controller="TimetableCtrl">
  <h2>You have taken {{ lunchCount }} times of PepperLunch</h2>
  <div class="btn btn-success" ng-click="increment()">+1</div>
</div>
```

4) Add the code to CoffeeScript

```
App.controller("TimetableCtrl", ["$scope", ($scope) ->
  $scope.lunchCount = 0

  $scope.increment = ->
    $scope.lunchCount++
])
```

## Successful Completion

- You should be able to change the counter upon click
- Learn how to use ng-controller
- Learn how to use ng-click
- Learn how to use Markup `{}` for string interpolation

## Reference Links

- [What does MVW stand for?](http://stackoverflow.com/questions/13329485/mvw-what-does-it-stand-for)
- [MVVW](https://plus.google.com/+AngularJS/posts/aZNVhj355G2)
