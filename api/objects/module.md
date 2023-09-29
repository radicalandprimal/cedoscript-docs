---
description: Module Object
---

# Module

## setToggled

```javascript
module.setToggled(false)

module.setToggled(true)
```

Sets the module to a new toggled state.

| Parameter | Type    | Description                 |
| --------- | ------- | --------------------------- |
| state     | Boolean | The new state of the module |

## toggle

```javascript
module.toggle()
```

Toggles the module

## toggleSilent

```javascript
module.toggleSilent()
```

Toggles the module without sending a notification

## isEnabled

```javascript
if(aura.isEnabled()){...

if(keystrokes.isEnabled()){...
```

Returns **true** if the module is enabled

## setKey

```javascript
module.setKey(code)
```

Sets the keybind to the new keycode

| Parameter | Type   | Description                        |
| --------- | ------ | ---------------------------------- |
| code      | Number | The new keybind code of the module |

## getName

```javascript
var modName = module.getName()
```

Returns the name of the module as a **String**

## getDescription

```javascript
var modDesc = module.getDescription()
```

Returns the description of the module as a **String**

## getKeybindCode

```javascript
var code = module.getKeybindCode()
```

Returns the current code of the keybind for the module as a **Number**

## Get Settings

These functions allow for getting settings within the module

{% hint style="info" %}
The only parameter is the setting name and it returns its respective [setting ](../settings.md)object
{% endhint %}

{% hint style="warning" %}
Will return null if the setting does not exist
{% endhint %}

```java
var numSetting = module.getNumberSetting(name)

var boolSetting = module.getBooleanSetting(name)

var modeSetting = module.getModeSetting(name)

var stringSetting = module.getStringSetting(name)

var multiBoolSetting = module.getMultiBoolSetting(name)

var colorSetting = module.getColorSetting(name)
```
