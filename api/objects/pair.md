---
description: When you want to store two objects together
---

# Pair

## Creation

{% hint style="info" %}
Make sure you import Pair by doing the following:

```javascript
var Pair = Java.type("dev.cedo.tuples.Pair")
```
{% endhint %}

```javascript
var Pair = Java.type("dev.cedo.tuples.Pair")

var script = initScript({
    name: "Test Script",
    description: "This is a test",
    author: "cedo"
})

var color1 = script.colorSetting("Color1", color({red: 255, green: 90, blue: 0}))
var color2 = script.colorSetting("Color2", color({red: 30, green: 190, blue: 90}))

script.onRender2D(function(event) {
    var customPair = Pair.of(color1.getColor(), color2.getColor())
})
```

## Functions

### of

```javascript
var customPair = Pair.of(color1.getColor(), color2.getColor())
//OR
var customPair = Pair.of(color1.getColor())
```

Will create a pair of the objects specified

### getFirst

```javascript
var firstObj = customPair.getFirst()
```

Returns the first object in the Pair

### getSecond

```javascript
var secondObj = customPair.getSecond()
```

Returns the second object in the Pair
