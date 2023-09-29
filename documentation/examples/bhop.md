---
description: Example of a vanilla bhop module.
---

# Bhop

```javascript
var script = initScript({
    name: "Bhop Test",
    description: "vanilla bhop",
    author: "life"
})

script.onMotion(function (event) {
    if (event.isPre() && player.onGround()) {
        player.jump()
    }
})
```
