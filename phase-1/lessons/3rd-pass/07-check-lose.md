# Check lose condition

- Board is full
- Cannot do the sum anymore

```
boardIsFull = (board) ->
  for row in board
    if $.inArray(0, row) > -1
      return false
  true

noValidMoves = (board) ->
  directions = ['up', 'down', 'left', 'right']

  for direction in directions
    newBoard = move(board, direction)
    return false if moveIsValid(newBoard, board)
  true

gameLost = (board) ->
  boardIsFull(board) && noValidMoves(board)
```
