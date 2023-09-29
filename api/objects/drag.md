---
description: This will explain how to create and use a Drag object
---

# Drag

A "drag" is an object that allows for dragging on the gui screen with objects and adaptively changes the x and y values.

These x and y values save and load in when you enable and disable a script.

## How to create a Drag object

```javascript
var drag = createDrag({
    initialX: 100,
    initialY: 100
})
```

### Parameters

| Parameter | Description                       |
| --------- | --------------------------------- |
| initialX  | The initial x value for the drag  |
| initialY  | The initial y value for the drag  |

{% hint style="info" %}
These values will be used when clicking the "Reset Draggables" button in the Gui Chat menu
{% endhint %}

## How to use the Drag object

First off you will want to create the Drag object and then in an event you **must** set the width and height of the drag, this allows for you to adaptively change the width and height of the Drag.

```javascript
var drag = createDrag({
    initialX: 100,
    initialY: 100
})

script.onRender2D(function (event) {
    drag.setWidth(100)
    drag.setHeight(100)

    render.drawRect(drag.getX(), drag.getY(), drag.getWidth(), drag.getHeight(), color({red: 255, green: 255, blue: 255}))
    
})
```

### Functions

| Function      | Description                                 |
| ------------- | ------------------------------------------- |
| `getX()`      | Gets the current x value of the Drag object |
| `getY()`      | Gets the current y value of the Drag object |
| `getWidth()`  | Gets the current width of the Drag object   |
| `getHeight()` | Gets the current height of the Drag object  |
| `setWidth()`  | Sets the width of the Drag object           |
| `setHeight()` | Sets the height of the Drag object          |
