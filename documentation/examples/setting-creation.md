---
description: >-
  Example usage of settings (note that you can put objects directly as
  parameters)
---

# Setting Creation

```javascript
var script = initScript({
    name: "Settings Example",
    description: "example of all settings",
    author: "life"
})

var modes = ["one", "two"]

var accent = color({
    red: 255,
    green: 70,
    blue: 0
})

var num = script.numberSetting("Number Setting name", 1, 1, 100, 1)

var string = script.stringSetting("String Setting name", "hello world")

var bool = script.booleanSetting("Boolean Setting name", false)

var mode = script.modeSetting("Mode Setting name", "one", modes)

var mode2 = script.modeSetting("Mode Setting2 name", "one", "one", "two")

var color = script.colorSetting("Color Setting name", accent)

var color2 = script.colorSetting("Color Setting2 name", 
color({ red: 255, green: 70, blue: 0 }))
```
