---
description: Displays how to apply a gradient to something
---

# Applying a gradient

```javascript
var script = initScript({    
    name: "test colors",    
    description: "This is the description",    
    author: "cedo"
})

script.onRender2D(function (event) {    
    var colors = client.getClientColors()    
    var white = color({ red: 255, green: 255, blue: 255 })
    var font = font.getMinecraftFontRenderer()    
    var textSize = font.getStringWidth(text)    
    var textHeight = font.getFontHeight()    
    
    render.applyGradient(300,300, textSize, textHeight, 1, colors.getFirst(), 
        colors.getFirst(), colors.getSecond(), colors.getSecond(), function () {       
            font.drawString("Cedo Moment", 300, 300, white)    
    })
})
```

<figure><img src="../../.gitbook/assets/Screenshot 2022-03-03 112909.png" alt=""><figcaption><p>Final result is a smooth gradient over some text</p></figcaption></figure>
