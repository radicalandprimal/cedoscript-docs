# FrameBuffer

## How to create

```javascript
var buffer = render.createFramebuffer()
```

To maintain the size of the framebuffer with the screen size you have to do the following code in Render2D

```javascript
var buffer = render.createFramebuffer()

script.onRender2D(function(event) {
    buffer.resize()
})
```

## Functions

### resize

```javascript
buffer.resize()
```

This updates the framebuffer size with the current screen size

### clear

```javascript
buffer.clear()
```

This clears the framebuffer

### bind

```javascript
buffer.bind()
```

Binds the framebuffer to what is rendering next

### unbind

```javascript
buffer.unbind()
```

Unbinds the framebuffer

### getTextureID

```javascript
var textureID = buffer.getTextureID()
```

Returns the texture ID as a Number

### getWidth

```javascript
var framebufferWidth = buffer.getWidth()
```

Returns the framebuffer width as a Number

### getHeight

```javascript
var framebufferHeight = buffer.getHeight()
```

Returns the framebuffer height as a Number
