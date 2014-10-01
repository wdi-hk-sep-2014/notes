# Generate Tile

- Random Index
- By definition, `Math.random()` will return value from 0 to 0.99... which is less than 1.

```
randomInt = (x) ->
  Math.floor(Math.random() * x)

randomCellIndices = ->
  [randomInt(4), randomInt(4)]
```

## Random Value

```
randomValue = ->
  values = [2, 2, 2, 4]
  val = values[randomIndex(values.length)]
```

## Generate Tile

- Assume it is giving value `2` right now, we will build a function in the future to generate `4` as well.
- Assume we always

```
generateTile = (board) ->
  value = 2
  [row, column] = randomCellIndices()

  if board[row][column] == 0
    board[row][column] = value
  else
    unless boardIsFull(board)
      generateTile(board)
```

## Show Board

```
showValue = (value) ->
  if value == 0 then "" else value

showBoard = (board) ->
  for r in [0..3]
    for c in [0..3]
      $(".r#{r}.c#{c} > div").html(showValue(board[r][c]))
```

## Bonus

```
getTileValue = ->
  values = [2, 2, 2, 4]
  val = values[Math.floor(Math.random() * values.length)]

value = getTileValue()
```