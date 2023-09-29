# Settings

## Global Functions

### getName

```javascript
var name = testSetting.getName()
```

Returns the name of the setting as a **String**

### **addParent**

```javascript
var showColors = script.booleanSetting("Show Colors", false)

var color1 = script.colorSetting("Color1", color({red: 255, green: 90, blue: 0}))
var color2 = script.colorSetting("Color2", color({red: 30, green: 190, blue: 90}))

color1.addParent(showColors, function (setting) {
    return setting.isEnabled()
})

color2.addParent(showColors, function (setting) {
    return setting.isEnabled()
})
```

Allows you to add a condition for the setting to show in the clickgui

![](<../.gitbook/assets/image (6).png>) ![The boolean setting determines if the color settings show](<../.gitbook/assets/image (4).png>)

## Number Setting

```javascript
var testSetting = script.numberSetting(name, defaultValue, min, max, increment)
```

`script.numberSetting(...` will return a number setting that allows for the following functions:

| Function             | Description                                               |
| -------------------- | --------------------------------------------------------- |
| `getValue()`         | Returns the current value of the setting as a **Double**. |
| `getMinValue()`      | Returns the min value of the setting as a **Number**.     |
| `getMaxValue()`      | Returns the max value of the setting as a **Number**.     |
| `getIncrement()`     | Returns the increment of the setting as a **Number**      |
| `setValue(newValue)` | Sets a new current value of the setting.                  |

The `getValue()` function returns a **Double**. The **Double** object allows for all sorts of different data types pertaining to numbers.\
\
You will be able to do the following functions:

* `getValue().floatValue()`
* `getValue().intValue()`
* `getValue().doubleValue()`
* `getValue().longValue()`

## Boolean Setting

```javascript
var testSetting = script.booleanSetting(name, value)
```

`script.booleanSetting(...` will return a boolean setting that allows for the following functions:

| Function          | Description                                                                                                            |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `isEnabled()`     | Returns the setting's state as a **boolean**.                                                                          |
| `toggle()`        | Changes the current state of the setting to the opposite. **i.e** _true_ turns to _false_ and _false_ turns to _true_. |
| `setState(state)` | Sets the current state of the boolean setting to the new state.                                                        |

## Mode Setting

```javascript
var testSetting = script.modeSetting(name, startMode, modes...)
```

### Modes Input

```javascript
var modes = ["One", "Two"]
var testSetting1 = script.modeSetting("Mode", "One", modes)

// OR

var testSetting2 = script.modeSetting("Mode", "One", "One", "Two")
```

`script.modeSetting(...` will return a mode setting that allows for the following functions:

| Function               | Description                                                                          |
| ---------------------- | ------------------------------------------------------------------------------------ |
| `setCurrentMode(mode)` | Sets the current mode (Parameter is a **String**)                                    |
| `is(mode)`             | Returns **True** if the current mode is equal to the specified mode in the parameter |
| `getMode()`            | Returns the current mode as a **String**                                             |

## Color Setting

```javascript
var testSetting = script.colorSetting(name, color)
```

### How to create a [Color object](broken-reference)

```javascript
var color = color({ 
    red: 1, 
    green: 1, 
    blue: 1 
})

var testSetting = script.colorSetting("Color one", color)

// OR

var testSetting = script.colorSetting("Color 2", 
color({ red: 1, green: 1, blue: 1, alpha: 210}))
```

`script.colorSetting(...` will return a color setting that allows for the following functions:

| Function          | Description                                                                                                                                 |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `getColor()`      | Returns the **`java.awt.Color`**object (This allows for other functions such as `getRGB()`, `geRed()`, `getBlue()`, `getGreen()`, and more) |
| `getHue()`        | Returns the hue of the current color as a **Number**.                                                                                       |
| `getSaturation()` | Returns the saturation of the current color as a **Number**.                                                                                |
| `isRainbow()`     | Returns **True** if the color setting is now a rainbow                                                                                      |
| `setRainbow(set)` | Sets the color setting to a rainbow if the parameter is true, sets the color setting back to a regular color picker if false                |
| `getRainbow()`    | Returns a [Rainbow ](objects/rainbow.md)object if the color setting is a rainbow, if it is not a rainbow then it is null                    |
| `getBrightness()` | Returns the brightness of the current color as a **Number**.                                                                                |

## String Setting

```javascript
var testSetting = script.stringSetting(name, containerString)
```

`script.stringSetting(...` will return a number setting that allows for the following functions:

| Function               | Description                                               |
| ---------------------- | --------------------------------------------------------- |
| `getString()`          | Returns the current **String** in the text box            |
| `setString(newString)` | Sets the current typed String to the new string parameter |

## Multi-Boolean Setting

```javascript
var testSetting = script.multiBoolSetting(name, booleanOptions...)

Boolean Inputs
var bools = ["One", "Two"]
var testSetting1 = script.multiBoolSetting("Options", bools)

// OR

var testSetting2 = script.multiBoolSetting("Options", "One", "Two")
```

`script.multiBoolSetting(...` will return a number setting that allows for the following functions:

| Function           | Description                                                                 |
| ------------------ | --------------------------------------------------------------------------- |
| `getSetting(name)` | Returns the sub boolean setting with the specified name                     |
| `isEnabled(name)`  | Returns **True** if the specified boolean setting with that name is enabled |
