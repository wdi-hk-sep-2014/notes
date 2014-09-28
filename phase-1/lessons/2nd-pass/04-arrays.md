# Arrays

```
# numeric array
myNumbers = [1, 2, 3, 4, 5, 6]
myNumbers[0]
myNumbers[1]
myNumbers.push(56)
myNumbers.pop()
myNumbers.pop()

# string array
myString = ["Welcome", "to"]
myString.shift()
myString.unshift(["Say", "hello"])
myString.pop()
myString.push("say")
myString.unshift("To")

# mixed-types array
myMixedArray = ["Welcome", 2, "course", 2014]

```

## Array Slicing

```
# ranges
a = [1..10]
a = [1...10]

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]

start   = numbers[0..2]

middle  = numbers[3...-2]

end     = numbers[-2..]

copy    = numbers[..]
```

## Pop in the middle / Splice
```
array = ['something', "Hello", "World", "Again", 'some others']
indexOfWorld = array.indexOf("World") will get the index of "World" or -1 if it doesn't exist. 
splicedElement = array.splice(indexOfWorld, 1) will remove "World" from the array.
```

## JavaScript Array

```
var a = [1, 2, 3]

var vegtables = ["Eggplants", "asparagus", "Lettuce"]

#Join an array
vegtables.join(", ")
>"Eggplants", "asparagus", "Lettuce"

#Pop an element off Array
vegtables.pop()

#Push an element onto a Array
vegtables.push("Avacado")
>3

v = vegtables.push("kale")
> ["Eggplants", "asparagus", "Lettuce", "Kale"]

#Array accessing
vegtables[0]
```

## Resources

Two most difficult parts in programming, include:

1. Having good naming convention
2. Array start with ZERO

- http://stackoverflow.com/questions/8205710/remove-a-value-from-an-array-in-coffeescript