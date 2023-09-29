---
description: Example of a success notification when the player jumps.
---

# Post Notification

```javascript
var script = initScript({
    name: "Notification Example",
    description: "Success Notification every frame where overall fps > 1000",
    author: "cedo"
})

script.onMotion(function (ev) {
    if (player.onGround()) {
        jumpAndPost()
    }
})

function jumpAndPost() {
    player.jump()
    notification.post(notification.success, "Jump", "Player had jumped")
}
```
