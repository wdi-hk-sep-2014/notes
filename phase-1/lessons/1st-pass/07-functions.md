# Functions

## Objective

To learn the structure, definition and usage of a CoffeeScript function.

## What are functions (Learning Objectives)

- Define a function
- Explain why you would use a function
- Inputs and Outputs (arguments)
- Why DRY code?

## How to define function?

1. Variable name (Function name)
2. Thin arrow (->)
3. Return result
4. Arguments (optional)

## How to use (call) a function?

1. Variable name (Function name)
2. Use parentheses () to call it
3. Pass in argument values

```
square = (x) -> x * x

cube   = (x) -> square(x) * x

area = (length, width) ->
  length * width

volume = (length, width, height) ->
  length * width * height

hello = (name) ->
  "Hello " + name

hello "Harry" #=> "Hello Harry"

hello2 = (nameArray) ->
  if nameArray.length >= 3
    "Hello #{nameArray[0]}, #{nameArray[1]} and #{nameArray[2]}"

hello2 ['Harry', 'Leo', 'Duck'] #=> "Hello Harry, Fer and Mark"
```

## With Default argument value

```
fill = (container, liquid = "coffee") ->
  "Filling the #{container} with #{liquid}..."
```

## Scope

Entering a function, is entering into another boundary

## Return

The last line of the CoffeeScript function will be returned to outer scope.

# Advanced Topics

## Function with multiple return values

```
weatherReport = (location) ->
  # Make an Ajax request to fetch the weather...
  [location, 72, "Mostly Sunny"]

[city, temp, forecast] = weatherReport "Berkeley, CA"
```

## JavaScript Functions

```
#first function
var first = function () { return vegtables[0]}

first()
> "Eggplant" 

#last function

function last () { return vegtables[vegtables.length - 1] };

vegtables.first = function () {return this[0] }
vegtables.last = function () { return this[this.length - 1 ] };
vegtables.last()

var f = function() { return this[1]};

vegtables.second = f

vegtables.second()
> "Radish"


fruits.second = vegtables.second
> value

fruits.second = vegtables.second()
```

# Code Challenge

1. [First Code Challenge in CoffeeScript](https://github.com/annieccheung/wdi3-hk-code-challenge)
2. [CoffeeScript Practice](https://gist.github.com/bridgpal/c2fbca5182b4d5e53caa)
3. [Good Programmig Style](http://www.cprogramming.com/tutorial/style.html)