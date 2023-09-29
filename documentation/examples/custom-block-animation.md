---
description: This page will explain how you can create a custom block hit animation
---

# Custom Block Animation

We have an event for this called the [CustomBlockRender ](../../api/events.md#custom-block-render)event that has a few functions in it. Something else we need to create a custom block animation is [GL11 ](../java-imports.md#gl11)for translating and rotating

## Example

```javascript
var GL11 = Java.type("org.lwjgl.opengl.GL11")

var script = initScript({
    name: "Butter Animation",
    description: "Adds the Butter block animation to Tenacity 5.0",
    author: "cedo"
})

var animationsMod = client.getModule("Animations")

script.onEnable(function() {
    //If Animations module is not toggled then we want to toggle it without
    // a notification
    if(!animationsMod.isEnabled()){
        animationsMod.toggleSilent()
    }
    //Set the animation mode to custom so that the onCustomBlockRender is called
    animationsMod.getModeSetting("Mode").setCurrentMode("Custom")
})

script.onCustomBlockRender(function (event) {
    //This is just some code customizing how the block animation is shown
    var swingProgress = event.getSwingProgress()
    var swingAnimation = Math.sin(Math.sqrt(swingProgress) * Math.PI);

    event.transformFirstPersonItem(event.getEquipProgress() * .5, 0);

    GL11.glRotated(-swingAnimation * -74.0 / 4.0, -8.0, -0.0, 9.0);
    GL11.glRotated(-swingAnimation * 15.0, 1.0, swingAnimation / 2.0, -0.0);
    event.doBlockTransformations()
    GL11.glTranslated(1.2, 0.3, 0.5);
    GL11.glTranslatef(-1.0, player.sneaking() ? -0.1 : -0.2, 0.2);

})
```
