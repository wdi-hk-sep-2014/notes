# Check move validity

```
arrayEqual = (a, b) ->
  for val, i in a
    if val != b[i]
      return false
  true

boardEqual = (a, b) ->
  for row, i in a
    unless arrayEqual(row, b[i])
      return false
  true

moveIsValid = (a, b) ->
  not boardEqual(a,b)
```