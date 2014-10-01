# Array / Board

- Long Version

```
board = []
for x in [0..3]
  board[x] = []
  for y in [0..3]
    board[x][y] = 0
```

- Short Version

```
@board = [0..3].map -> [0..3].map -> 0
```

## Build Board

```
buildBoard = ->
  [0..3].map -> [0..3].map -> 0
```

## Debugging Helper Tool

```
ppArray = (a) ->
  for row in a
    console.log row
```