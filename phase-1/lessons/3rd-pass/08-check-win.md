# Check win condition

- When one of the tiles goes up to 2048, shows win message

```
gameWon = (board) ->
  for row in board
    for cell in row
      if cell >= WinningTileValue
        return true
  false
```
