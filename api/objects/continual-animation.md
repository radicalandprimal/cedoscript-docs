---
description: This page explains the Continual Animation object
---

# Continual Animation

This object allows you to animate to certain endpoints

## How to create

```javascript
var anim = render.newContinualAnimation()

script.onRender2D(function(event) {
    
})
```

## Functions

### animate

```javascript
anim.animate(endpoint, ms)
```

| Parameter | Type   | Description                    |
| --------- | ------ | ------------------------------ |
| endpoint  | Number | The endpoint of the animation  |
| ms        | Number | Milliseconds of animation time |

### getOutput

```javascript
anim.getOutput()
```

Returns the animation output as a Number

## Usage

Used for health animation of a target

```javascript
var anim = render.newContinualAnimation()

script.onRender2D(function (event) {
    var target = client.getAuraTarget()
    if (!target) return null
    var healthbarWidth = 100
    var healthPercentage = target.getHealth() / target.getMaxHealth()
    
    anim.animate(healthbarWidth * healthPercentage, 18)

    render.drawRect(100, 100, anim.getOutput(), 80, color({red: 255, green: 255, blue: 255}))

})
```
