---
description: Information about the font binding
---

# Font

The following functions allow you to get an AbstractFontRenderer object which allows for some more functions to be used

{% hint style="info" %}
To make use of **Bold** fonts just use the minecraft formatting code for bold `§l`

See more about formatting codes here: [formatting codes](https://minecraft.fandom.com/el/wiki/Formatting\_codes)
{% endhint %}

## Functions

### drawString

```javascript
font.getMinecraftFontRenderer().drawString(text, x, y, color)

//or

font.getTenacityFont14().drawString(text, x, y, color)
```

Draws a string in the specified x and y values with the specified color

| Parameter | Type                             | Description       |
| --------- | -------------------------------- | ----------------- |
| text      | String                           | Text to draw      |
| x         | Number                           | X pos of the text |
| y         | Number                           | Y pos of the text |
| color     | [Color](../api/objects/color.md) | Color of the text |

### drawStringWithShadow

```javascript
font.getMinecraftFontRenderer().drawStringWithShadow(text, x, y, color)

//or

font.getTenacityFont14().drawStringWithShadow(text, x, y, color)
```

Draws a string with a shadow in the specified x and y values with the specified color

| Parameter | Type                             | Description       |
| --------- | -------------------------------- | ----------------- |
| text      | String                           | Text to draw      |
| x         | Number                           | X pos of the text |
| y         | Number                           | Y pos of the text |
| color     | [Color](../api/objects/color.md) | Color of the text |

### drawCenteredString

```javascript
font.getMinecraftFontRenderer().drawCenteredString(text, x, y, color)

//or

font.getTenacityFont14().drawCenteredString(text, x, y, color)
```

Draws a centered string in the specified x and y values with the specified color

| Parameter | Type                             | Description       |
| --------- | -------------------------------- | ----------------- |
| text      | String                           | Text to draw      |
| x         | Number                           | X pos of the text |
| y         | Number                           | Y pos of the text |
| color     | [Color](../api/objects/color.md) | Color of the text |

### getStringWidth

```javascript
font.getMinecraftFontRenderer().getStringWidth(text)

//or

font.getTenacityFont14().getStringWidth(text)
```

Returns a **Number** that is the string width based on the specified text



| Parameter | Type   | Description                                   |
| --------- | ------ | --------------------------------------------- |
| text      | String | Specified text to use to get the string width |

### getHeight

```javascript
font.getMinecraftFontRenderer().getHeight()

//or

font.getTenacityFont14().getHeight()
```

Returns a **Number** based on the font's height

### getMiddleOfBox

```javascript
font.getMinecraftFontRenderer().getMiddleOfBox(height)

//or

font.getTenacityFont14().getMiddleOfBox(height)
```

Returns a **Number** that should be the font's Y center of the height

## getMinecraftFontRenderer

```javascript
font.getMinecraftFontRenderer().drawString(...
```

## getTenacityFont14

```javascript
font.getTenacityFont14().drawString(...
```

## getTenacityFont16

```javascript
font.getTenacityFont16().drawString(...
```

## getTenacityFont18

```javascript
font.getTenacityFont18().drawString(...
```

## getTenacityFont20

```javascript
font.getTenacityFont20().drawString(...
```

## getTenacityFont22

```javascript
font.getTenacityFont22().drawString(...
```

## getTenacityFont24

```javascript
font.getTenacityFont24().drawString(...
```

## getTenacityFont26

```javascript
font.getTenacityFont26().drawString(...
```

## getTenacityFont28

```javascript
font.getTenacityFont28().drawString(...
```

## getTenacityFont32

```javascript
font.getTenacityFont32().drawString(...
```

## getTenacityFont40

```javascript
font.getTenacityFont40().drawString(...
```

## getTenacityFont80

```javascript
font.getTenacityFont80().drawString(...
```
