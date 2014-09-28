# Array / Board

- Short Version

```
@board = [0..3].map -> [0..3].map -> 0
```

- Long Version

```
board = []
for x in [0..3]
  board[x] = []
  for y in [0..3]
    board[x][y] = 0
```