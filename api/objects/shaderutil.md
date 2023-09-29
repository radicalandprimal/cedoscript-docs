# ShaderUtil

## How to create

```javascript
var shaderUtil = render.createShaderUtil(getFragSource())
```

You must input a String of the Fragment shader

## Functions

### init

```javascript
shaderUtil.init()
```

Initializes the shader

### unload

```javascript
shaderUtil.unload()
```

Unloads the shader

### setUniformf

```javascript
shaderUtil.setUniformf(name args...)
```

Sets specified uniform to the specified arguments

| Name | Type   | Description                                           |
| ---- | ------ | ----------------------------------------------------- |
| name | String | Name of the uniform                                   |
| args | Number | These can be up to 4 arguments of non integer numbers |

### setUniformi

```javascript
shaderUtil.setUniformf(name args...)
```

| Name | Type   | Description                            |
| ---- | ------ | -------------------------------------- |
| name | String | Name of the uniform                    |
| args | Number | These can be up to 2 integer arguments |

### drawQuads

```javascript
shaderUtil.drawQuads()
//OR
shaderUtil.drawQuads(x, y, width, height)
```

You can draw over the whole screen or in a specified position and size

#### Optional

| Name   | Type   | Description             |
| ------ | ------ | ----------------------- |
| x      | Number | X position of the quads |
| y      | Number | Y position of the quads |
| width  | Number | Width of the quads      |
| height | Number | Height of the quads     |
