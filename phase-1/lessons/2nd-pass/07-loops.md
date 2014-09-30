# Loops

```
list = [1..10]

for count in list
  console.log count

countdown = (num for num in [10..1])

yearsOld = max: 10, ida: 9, tim: 11

ages = for child, age of yearsOld
  "#{child} is #{age}"
```

## While

```
# Econ 101
if this.studyingEconomics
  buy()  while supply > demand
  sell() until supply > demand

# Nursery Rhyme
num = 6
lyrics = while num -= 1
  "#{num} little monkeys, jumping on the bed.
    One fell out and bumped his head."
```

## Specific use

```
# The first ten global properties.

globals = (name for name of window)[0...10]
```

## JavaScript Loops

```
#for loops
for (var i = 0, i < fruits.length ; i += 1) {
  console.log(fruit[i]);
}

#while loops
while (i < fruits.length ) {
  console.log(fruits[i]); i += 1;
}
```

## Resources

- [For Quiz](https://gist.github.com/harryworld/96db1a608cf84be2eb85)