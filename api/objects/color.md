# Color

## Creation

```javascript
var color = color({ red: 236, green: 143, blue: 209 })

// OR

var color = color({ red: 236, green: 143, blue: 209, alpha: 120 })

//OR

var color = color({ hex:0xff00ff00 }) // Green
var color = color({ hex: -1 }) //White
```

Returns a `java.awt.Color` object

## Functions

### getRGB

```javascript
color.getRGB()
```

Returns the color as an int instead of the `java.awt.Color` object
