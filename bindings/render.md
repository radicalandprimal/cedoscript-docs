---
description: Information about the render binding
---

# Render

## drawRect

```javascript
render.drawRect(x, y, width, height, color)
```

Renders a rectangle using the specified parameters

| Parameter | Type                             | Description        |
| --------- | -------------------------------- | ------------------ |
| x         | Number                           | X pos of the rect  |
| y         | Number                           | Y pos of the rect  |
| width     | Number                           | Width of the rect  |
| height    | Number                           | Height of the rect |
| color     | [Color](../api/objects/color.md) | Color of the rect  |



## drawRoundedRect

```javascript
render.drawRoundedRect(x, y, width, height, radius, color)
```

Renders a rounded rectangle

| Parameter | Type                             | Description                 |
| --------- | -------------------------------- | --------------------------- |
| x         | Number                           | X pos of the rect           |
| y         | Number                           | Y pos of the rect           |
| width     | Number                           | Width of the rect           |
| height    | Number                           | Height of the rect          |
| radius    | Number                           | Radius of the rounded parts |
| color     | [Color](../api/objects/color.md) | Color of the rect           |

## drawGradientRect

```javascript
render.drawGradientRect(x, y, width, height, alpha, bottomLeft, topLeft, bottomRight, topRight)
```

Draws a gradient with values for all corners of a rectangle

| Parameter   | Type                             | Description                      |
| ----------- | -------------------------------- | -------------------------------- |
| x           | Number                           | X pos of the rect                |
| y           | Number                           | Y pos of the rect                |
| width       | Number                           | Width of the rect                |
| height      | Number                           | Height of the rect               |
| alpha       | Number                           | Alpha of the gradient            |
| bottomLeft  | [Color](../api/objects/color.md) | Color of the bottom left corner  |
| topLeft     | [Color](../api/objects/color.md) | Color of the top left corner     |
| bottomRight | [Color](../api/objects/color.md) | Color of the bottom right corner |
| topRight    | [Color](../api/objects/color.md) | Color of the top right corner    |

### drawGradientRectHorizontal

```javascript
render.drawGradientRectHorizontal(x, y, width, height, alpha, left, right)
```

Draws a gradient horizontally (left to right)

| Parameter | Type                             | Description             |
| --------- | -------------------------------- | ----------------------- |
| x         | Number                           | X pos of the rect       |
| y         | Number                           | Y pos of the rect       |
| width     | Number                           | Width of the rect       |
| height    | Number                           | Height of the rect      |
| alpha     | Number                           | Alpha of the gradient   |
| left      | [Color](../api/objects/color.md) | Color of the left side  |
| right     | [Color](../api/objects/color.md) | Color of the right side |

### drawGradientRectVertical

```javascript
render.drawGradientRectVertical(x, y, width, height, alpha, top, bottom)
```

Draws a gradient vertically (top to bottom)

| Parameter | Type                             | Description              |
| --------- | -------------------------------- | ------------------------ |
| x         | Number                           | X pos of the rect        |
| y         | Number                           | Y pos of the rect        |
| width     | Number                           | Width of the rect        |
| height    | Number                           | Height of the rect       |
| alpha     | Number                           | Alpha of the gradient    |
| top       | [Color](../api/objects/color.md) | Color of the top side    |
| bottom    | [Color](../api/objects/color.md) | Color of the bottom side |

## drawGradientRoundedRect

```javascript
render.drawGradientRoundedRect(x, y, width, height, radius, bottomLeft, topLeft, bottomRight, topRight)
```

Draws a rounded gradient with values for all corners of a rectangle

| Parameter   | Type                             | Description                      |
| ----------- | -------------------------------- | -------------------------------- |
| x           | Number                           | X pos of the rect                |
| y           | Number                           | Y pos of the rect                |
| width       | Number                           | Width of the rect                |
| height      | Number                           | Height of the rect               |
| radius      | Number                           | Radius of the rounded rect       |
| bottomLeft  | [Color](../api/objects/color.md) | Color of the bottom left corner  |
| topLeft     | [Color](../api/objects/color.md) | Color of the top left corner     |
| bottomRight | [Color](../api/objects/color.md) | Color of the bottom right corner |
| topRight    | [Color](../api/objects/color.md) | Color of the top right corner    |

### drawGradientRoundHorizontal

```javascript
render.drawGradientRoundHorizontal(x, y, width, height, radius, left, right)
```

Draws a rounded gradient horizontally (left to right)

| Parameter | Type                             | Description                |
| --------- | -------------------------------- | -------------------------- |
| x         | Number                           | X pos of the rect          |
| y         | Number                           | Y pos of the rect          |
| width     | Number                           | Width of the rect          |
| height    | Number                           | Height of the rect         |
| radius    | Number                           | Radius of the rounded rect |
| left      | [Color](../api/objects/color.md) | Color of the left side     |
| right     | [Color](../api/objects/color.md) | Color of the right side    |

### drawGradientRoundVertical

```javascript
render.drawGradientRoundVertical(x, y, width, height, radius, top, bottom)
```

Draws a rounded gradient horizontally (top to bottom)

| Parameter | Type                             | Description                |
| --------- | -------------------------------- | -------------------------- |
| x         | Number                           | X pos of the rect          |
| y         | Number                           | Y pos of the rect          |
| width     | Number                           | Width of the rect          |
| height    | Number                           | Height of the rect         |
| radius    | Number                           | Radius of the rounded rect |
| top       | [Color](../api/objects/color.md) | Color of the top side      |
| bottom    | [Color](../api/objects/color.md) | Color of the bottom side   |

## applyGradient

```javascript
render.applyGradient(x, y, width, height, alpha, bottomLeft, topLeft, bottomRight, topRight, function() {
    ...
    (Render stuff here) 
    ...
})
```

Applies a gradient to any rendered object in the callback function

| Parameter         | Type                             | Description                                                                                      |
| ----------------- | -------------------------------- | ------------------------------------------------------------------------------------------------ |
| x                 | Number                           | X pos of the rect                                                                                |
| y                 | Number                           | Y pos of the rect                                                                                |
| width             | Number                           | Width of the rect                                                                                |
| height            | Number                           | Height of the rect                                                                               |
| alpha             | Number                           | Alpha of the final result                                                                        |
| bottomLeft        | [Color](../api/objects/color.md) | Color of the bottom left corner                                                                  |
| topLeft           | [Color](../api/objects/color.md) | Color of the top left corner                                                                     |
| bottomRight       | [Color](../api/objects/color.md) | Color of the bottom right corner                                                                 |
| topRight          | [Color](../api/objects/color.md) | Color of the top right corner                                                                    |
| callback function | Function                         | create a function here to specify a specific group of objects for the gradient to be applied too |

## interpolateColors

```javascript
var interpolatedColor = render.interpolateColors(colorOld, colorNew, percentage)
```

Returns a an interpolated [Color ](../api/objects/color.md)between the two colors based on the percentage

| Parameter  | Type                             | Description                     |
| ---------- | -------------------------------- | ------------------------------- |
| colorOld   | [Color](../api/objects/color.md) | Original color                  |
| colorNew   | [Color](../api/objects/color.md) | New color to be interpolated to |
| percentage | Number                           | Percentage to interpolate with  |

## applyOpacity

```javascript
var color = client.getClientColors().getFirst()
var alpha = .5
var opaqueColor = render.applyOpacity(color, alpha)
```

Applies opacity to a color with a value ranging from 0-1

| Parameter | Type                             | Description                  |
| --------- | -------------------------------- | ---------------------------- |
| color     | [Color](../api/objects/color.md) | Original color               |
| alpha     | Number                           | Alpha value of the new color |

## getScaledWidth

```javascript
render.getScaledWidth()
```

Returns the scaled width of the screen as a **Number**

## getScaledHeight

```javascript
render.getScaledHeight()
```

Returns the scaled height of the screen as a **Number**

## drawEntity3D

```javascript
render.drawEntity3D(x, y, scale, yaw, pitch, entity)
```

| Parameter | Type                                                   | Description         |
| --------- | ------------------------------------------------------ | ------------------- |
| x         | Number                                                 | X pos of the entity |
| y         | Number                                                 | Y pos of the entity |
| scale     | Number                                                 | Scale of the entity |
| yaw       | Number                                                 | Yaw of the entity   |
| pitch     | Number                                                 | Pitch of the entity |
| entity    | [EntityLivingBase](../api/objects/entitylivingbase.md) | Entity to render    |

## drawEntity2D

```javascript
render.drawEntity2D(x, y, width, height, entity)
```

Draws the entity's head

| Parameter | Type                                                   | Description                 |
| --------- | ------------------------------------------------------ | --------------------------- |
| x         | Number                                                 | X pos of the entity's head  |
| y         | Number                                                 | Y pos of the entity's head  |
| width     | Number                                                 | Width of the entity's head  |
| height    | Number                                                 | Height of the entity's head |
| entity    | [EntityLivingBase](../api/objects/entitylivingbase.md) | Entity to render            |

## newContinualAnimation

```javascript
var anim = render.newContinualAnimation()
```

Returns a new [Continual Animation](../api/objects/continual-animation.md) object

## createFramebuffer

```javascript
var buffer = render.createFramebuffer()
```

Returns a new [Framebuffer](../api/objects/framebuffer.md) object

## drawBoundingBox

```javascript
render.drawBoundingBox(entity, color)
```

This renders the entity's bounding box with the specified color

| Parameter | Type                                                   | Description                          |
| --------- | ------------------------------------------------------ | ------------------------------------ |
| entity    | [EntityLivingBase](../api/objects/entitylivingbase.md) | Entity to render the bounding box on |
| color     | Color                                                  | Color of the bounding box            |

## scissorStart

```javascript
render.scissorStart(x, y, width, height)
```

This is a helper function for scissoring out stuff

| Parameter | Type   | Description                   |
| --------- | ------ | ----------------------------- |
| x         | Number | The x position of the scissor |
| y         | Number | The y position of the scissor |
| width     | Number | The width of the scissor      |
| height    | Number | The height of the scissor     |

## scissorEnd

```javascript
render.scissorEnd()
```

Disables the scissor test

## getPartialTicks

```javascript
var ticks = render.getPartialTicks()
```

Gets the render partial ticks as a Number

## bindMinecraftFramebuffer

```javascript
render.bindMinecraftFramebuffer()
```

This rebinds the Minecraft framebuffer so you can continue rendering after using other [Framebuffer ](broken-reference)objects

## createShaderUtil

```javascript
var shader = render.createShaderUtil(fragSource)
```

Returns a [ShaderUtil ](../api/objects/shaderutil.md)object

| Name       | Type   | Description                         |
| ---------- | ------ | ----------------------------------- |
| fragSource | String | The complete fragment shader source |
