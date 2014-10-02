# Move

- We will need 4 directions, up / down / left / right
- Make use of jQuery `keypress()`, and check the key ASCII code.

## Steps

1. Deal with horizontal move first, get the rows
  - getRow
2. Merge the cells, handle moving `right`, `down` first
  - mergeCells
  - merge
3. Collapse the cells by removing `0`, handle `right`, `down` first
  - collapseCells
4. Set the rows
  - setRow
5. Repeat merging for `left`, `up`
  - mergeCells
  - collapseCells
6. Repeat the above with the vertical move
  - getColumn
  - setColumn

```
move = (board, direction) ->

  newBoard = buildBoard()

  for i in [0..3]
    switch direction
      when 'right', 'left'
        row = mergeCells(getRow(i, board), direction)
        row = collapseCells(row, direction)
        setRow(row, i, newBoard)
      when 'up', 'down'
        column = mergeCells(getColumn(i, board), direction)
        column = collapseCells(column, direction)
        setColumn(column, i, newBoard)
  newBoard
```

## Get Row (Column)

```
getRow = (rowNumber, board) ->
  [r, b] = [rowNumber, board]
  [b[r][0], b[r][1], b[r][2], b[r][3]]
```

## Merge Cells

- To compare cells 
- if they are having same values,
  - merge them (multiply)
- if not
  - skip

```
mergeCells = (cells, direction) ->

  merge = (cells) ->
    for i in [3...0]
      for j in [i-1..0]
        [n, m] = [cells[i], cells[j]]

        if n == 0 then break
        else if n == m
          cells[i] *= 2
          cells[j] = 0
          break
        else if m != 0 then break

    cells

  switch direction
    when 'right', 'down'
      cells = merge cells
    when 'left', 'up'
      cells = merge(cells.reverse()).reverse()
  cells
```

## Collapse Cells

- Trim the `0` and pack them together

```
collapseCells = (cells, direction) ->

  cells = cells.filter (x) -> x != 0
  padding = 4 - cells.length

  for i in [0...padding]
    switch direction
      when 'right', 'down' then cells.unshift 0
      when 'left', 'up' then cells.push 0
  cells
```

## Set Row (Column)

```
setRow = (row, rowNumber, board) ->
  board[rowNumber] = row
```
