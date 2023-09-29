---
description: This shows how to create a gradient rounded rectangle from corner to corner
---

# Gradient Round Rectangle

```javascript
var script = initScript({
   name: "test colors",
   description: "This is the description",    
   author: "cedo"
   })
   
script.onRender2D(function (event) {    
   var colors = client.getClientColors()    
   var middleColor = render.interpolateColors(colors[0], colors[1], 0.5)   
 
   render.drawGradientRoundedRect(300, 300, 100, 100, 6, middleColor, colors[0], colors[1], middleColor)
})
```

<figure><img src="../../.gitbook/assets/Screenshot 2022-03-03 111007.png" alt=""><figcaption><p>Draws a gradient rounded rectangle with the client colors</p></figcaption></figure>
