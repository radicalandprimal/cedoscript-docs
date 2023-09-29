---
description: Where your script code goes to be run at a certain time
---

# Events

## Info

### How to cancel an event

```javascript
event.cancel() 
```

This will cancel the event.

## Enable

```javascript
script.onEnable(function () {...
```

This event will be called every time the script is enabled.

## Disable

```javascript
script.onDisable(function () {...
```

This event will be called every time the script is disabled.

## Packet Events

#### Functions

Both packet events have this function

| Function        | Description                                                                                                                                    |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `getPacketID()` | <p>Returns the packet ID as a <strong>Number</strong><br>(Should be used for comparison with a <a href="../bindings/packet.md">packet</a>)</p> |

### Packet Send

```javascript
script.onPacketSend(function (event) {...
```

Called before packets are sent to server.

### ​Packet Receive​ <a href="#packet-receive" id="packet-receive"></a>

```javascript
script.onPacketReceive(function (event) {...
```

Called on packets received, before the client handles them.

## Tick

```javascript
script.onTick(function (event) {...
```

Called on each tick.

## Motion

```javascript
script.onMotion(function (event) {...
```

Called on motion updates.

### Functions

| Function                   | Description                                        |
| -------------------------- | -------------------------------------------------- |
| `setX(x)`                  | Sets the players x position using the event        |
| `setY(y)`                  | Sets the players y position using the event        |
| `setZ(z)`                  | Sets the players z position using the event        |
| `getX()`                   | Returns the current x pos of the player            |
| `getY()`                   | Returns the current y pos of the player            |
| `getZ()`                   | Returns the current z pos of the player            |
| `isOnGround()`             | Returns **true** the player is on ground           |
| `setGround(ground)`        | Sets the player's on ground state to the new state |
| `getYaw()`                 | Returns the players yaw as a **Number**            |
| `setYaw(yaw)`              | Sets the players yaw using the event               |
| `getPitch()`               | Returns the players pitch as a **Number**          |
| `setPitch(pitch)`          | Sets the players pitch using the event             |
| `isPre()`                  | Returns **true** the event is onPre                |
| `isPost()`                 | Returns **true** the event is onPost               |
| `setRotations(yaw, pitch)` | Sets the players yaw and pitch at the same time    |

## Move

```javascript
script.onMove(function (event) {...
```

Called when a player is moving.

| Function          | Description                                 |
| ----------------- | ------------------------------------------- |
| `setX(x)`         | Sets the players x position using the event |
| `setY(y)`         | Sets the players y position using the event |
| `setZ(z)`         | Sets the players z position using the event |
| `getX()`          | Returns the current x pos of the player     |
| `getY()`          | Returns the current y pos of the player     |
| `getZ()`          | Returns the current z pos of the player     |
| `setSpeed(speed)` | sets the the speed of the player            |

## Render 3D

```javascript
script.onRender3D(function (event) {...
```

Called on the rendering of 3D objects.

### Functions

| Function     | Description                               |
| ------------ | ----------------------------------------- |
| `getTicks()` | Returns the event's ticks as a **Number** |

## Render 2D

```javascript
script.onRender2D(function (event) {...
```

Called on the rendering of 2D objects.

| Function      | Description                                          |
| ------------- | ---------------------------------------------------- |
| `getWidth()`  | Returns the scaled resolution width as a **Number**  |
| `getHeight()` | Returns the scaled resolution height as a **Number** |

## Shader

```javascript
script.onShader(function (ev) {...
```

Everything in this event will be blurred when PostProcessing module is enabled and blur or bloom is enabled. You can tell if Bloom is enabled by using the following functions

| Function    | Description                          |
| ----------- | ------------------------------------ |
| `isBloom()` | Returns **True** if bloom is enabled |

## ChatReceivedEvent

```javascript
script.onChatReceived(function (ev) {...
```

This event is called every time a message is received in the chat

### Functions

| Function          | Description                                      |
| ----------------- | ------------------------------------------------ |
| `getRawMessage()` | Returns the raw received message as a **String** |

## PlayerSendMessage

```javascript
script.onPlayerSendMessage(function (ev) {...
```

This event is called every time the player (i.e. the one using the script) sends a message in the chat

### Functions

| Function       | Description                         |
| -------------- | ----------------------------------- |
| `getMessage()` | Returns the message as a **String** |

## WorldLoad

```javascript
script.onWorldLoad(function (ev) {...
```

This event is called when a world is loaded in

## Custom Block Render

```javascript
script.onCustomBlockRender(function (ev) {...
```

This event is called when Animations is toggled and the mode is set to custom

| Function                                                                                       | Description                                                                     |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `getSwingProgress()`                                                                           | Returns the swing progress as a Number                                          |
| `getEquipProgress()`                                                                           | Returns the equip progress as a Number                                          |
| `doBlockTransformations()`                                                                     | Normalizes the translation of where the block should be                         |
| <p><code>transformFirstPersonItem(</code></p><p><code>equipProgress, swingprogress)</code></p> | Performs transformations prior to the rendering of a held item in first person. |

{% hint style="info" %}
See [How to create a custom block animation](broken-reference)
{% endhint %}

## Render Model

```javascript
script.onRenderModel(function (ev) {...
```

This event is called when an entity is rendered. on Pre before entity is rendered and on post after entity is rendered.

| Function       | Description                                                                                            |
| -------------- | ------------------------------------------------------------------------------------------------------ |
| `getEntity()`  | Returns an [EntityLivingBase ](objects/entitylivingbase.md)object of the entity that is being rendered |
| `drawModel()`  | Draws the entity model                                                                                 |
| `drawLayers()` | Draws extra layers i.e. swords                                                                         |

## Attack

```javascript
script.onAttack(function (ev) {...
```

This event is called when you are attacking an entity

| Function            | Description                                                                                            |
| ------------------- | ------------------------------------------------------------------------------------------------------ |
| `getTargetEntity()` | Returns an [EntityLivingBase ](objects/entitylivingbase.md)object of the entity that is being attacked |
