# Debugging

## Start

```
console.log('Hello World!')
console.error('Error happens!!!')

console.group('Group started')
console.log('Start 1')
console.log('Start 2')
console.groupEnd()

# String substitution
console.log("%s has %d points", "Sam", "100")
```

## Selecting Elements with jQuery

```
$('.master')
```

## Debugger

### Setting breakpoints in JavaScript

```
var area = function() {
  debugger;
  var width = 10;
  var height = 10;
  console.log("Area will be %d", width * height);
}
area();
```

To enter a multi-line expression at the shell prompt (such as a function definition) press `Shift` + `Enter`  between lines.

## Elements

- Add / Modify Attribute
- Edit as HTML
- Delete Node
- Change CSS

## Sources

You can view all of your main document's resources, including images, scripts, and fonts, and those of any loaded frames. The top level category of page resources are the document's frames, which includes the main document, and its embedded frames.

## Network

The Network panel provides insights into resources that are requested and downloaded over the network in real time. Identifying and addressing those requests taking longer than expected is an essential step in optimizing your page.

## Other Stuff

- Settings
  - Disable JavaScript
  - Default Indentation
- Emulation
  - Mobile View
  - Device
  - Screen
  - User Agent

# Resources

- https://developer.chrome.com/devtools/index