---
description: This object can be used when a color setting is set to rainbow
---

# Rainbow

## Functions

### getColor

```javascript
var rainbowColor = rainbow.getColor()

//This returns rainbow's color using an index of the rainbow
var rainbowColor2 = rainbow.getColor(80)
```

Returns a `Java.awt.Color` object of the rainbow's color

### getSaturation

```javascript
var saturation = rainbow.getSaturation()
```

Returns a **Number** from 0-1 on how much the rainbow is saturated

### getSpeed

```javascript
var speed = rainbow.getSpeed()
```

Returns a **Number** on how fast the rainbow is going (lower values are faster)

### setSaturation

```javascript
rainbow.setSaturation(sat)
```

Sets the saturation of the rainbow (Values should be between 1-0)

### setSpeed

```javascript
rainbow.setSpeed(speed)
```

Sets the speed of the rainbow (lower values are faster)
