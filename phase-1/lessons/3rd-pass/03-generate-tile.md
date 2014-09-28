# Generate Tile

- Random Index
- By definition, `Math.random()` will return value from 0 to 0.99... which is less than 1.

```
randomIndex = (x) ->
  Math.floor(Math.random() * x)
```

- Random Value

```
randomValue = ->
  values = [2, 2, 2, 4]
  val = values[randomIndex(values.length)]
```

