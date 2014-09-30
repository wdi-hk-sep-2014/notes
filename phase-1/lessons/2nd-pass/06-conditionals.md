# Conditionals

```
mood = greatlyImproved if singing

if happy and knowsIt
  console.log "That's nice"
else
  console.log "Show it"

date = if friday then sue else jill
```

## Ternary

```
eldest = if 24 > 21 then "Liz" else "Ike"
```

## Switch

```
switch day
  when "Mon" then go work
  when "Tue" then go relax
  when "Thu" then go iceFishing
  when "Fri", "Sat"
    if day is bingoDay
      go bingo
      go dancing
  when "Sun" then go church
  else go work
```

## JavaScript Conditionals

```
if (i > 7) { 
    console.log("Hello") 
} 
else if (i < 3) {
    console.log("Goodbye")
} 
else { 
    console.log("between 3 and 7 (inclusive)");
}


a = {x: 5, y: 7, area_multiplier: function (multiple) {return this.x * this.y * multiple} };
```

## Quick Challenges

- [checkBaggage](https://gist.github.com/mddub/d64f7d04f35bc78e2004)

## Resources

- [Truthy vs True Example](http://stackoverflow.com/questions/8127883/easiest-way-to-check-if-string-is-null-or-empty)
- [JavaScript (== vs ===)](http://stackoverflow.com/questions/359494/does-it-matter-which-equals-operator-vs-i-use-in-javascript-comparisons)