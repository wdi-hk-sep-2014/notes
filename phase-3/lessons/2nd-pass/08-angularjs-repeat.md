# AngularJS (ng-repeat)

The ngRepeat directive instantiates a template once per item from a collection. Each template instance gets its own scope, where the given loop variable is set to the current collection item, and $index is set to the item index or key.

## Objective

To simpify the process of templating, minimize the line number of codes for the lunch board.

## Steps

1) Take a look on the pattern on the board, it is two levels of for loop

2) Create the arrays in CoffeeScript, which will be used by the loop

```
  $scope.weeks = [1..13]
```

3) Remove most of the rows in HTML, leaving only one, and start adding `ng-repeat`

```html
<div class="row week" ng-repeat="week in weeks">
```

4) Change the week number using `$index`

```html
<div class="col-md-2 number">Week {{ $index + 1 }}</div>
```

5) Switch the array in CoffeeScript into two levels, by adding initialization to the values

```
  $scope.init = ->
    for i in [1..13]
      $scope.weeks.push [0, 0, 0, 0, 0]

  $scope.init()
```

6) Remove most of the cells, and use `ng-repeat` as well

```html
<div class="col-md-2 day" ng-repeat="day in week">
```

7) Use the button inside the board in increment the counter

```
<div class="btn btn-success" ng-click="increment()"></div>
```

8) Improve programming logic to store the clicked value on each day, by passing the current index

```
<div class="btn btn-success" ng-click="increment($parent.$index, $index)"></div>
```

9) In CoffeeScript, take the two arguments as `week` and `day`, representing the indexes of the two-level array

```
  $scope.increment = (week, day) ->
    if $scope.weeks[week][day] is 0
      $scope.lunchCount++
      $scope.weeks[week][day] = 1
    else
      $scope.lunchCount--
      $scope.weeks[week][day] = 0
```

10) Modify the class to show differently for selected state, using `ng-class`

```html
<div class="btn btn-success" ng-class="getClass(day)" ng-click="increment($parent.$index, $index)"></div>
```

11) Add the `getClass()` method back to controller

```
  $scope.getClass = (day) ->
    if day is 0 then 'btn-success' else 'btn-danger'
```

## Successful Completion

- Use `ng-repeat` to show the whole board
- Click on anyone button to increment the counter
- The color of button would change upon click

## Reference Links

- [ng-repeat directive](https://docs.angularjs.org/api/ng/directive/ngRepeat)
