---
description: Information about the client binding
---

# Client

## getClientVersion

```javascript
var version = client.getClientVersion()
```

Returns a **String** with something like "5.0" or "5.0 (Beta)"

## leftMouseButtonDown

```javascript
var leftMouse = client.leftMouseButtonDown()
```

Returns true if the left mouse button is down

## rightMouseButtonDown

```javascript
var rightMouse = client.rightMouseButtonDown()
```

Returns true if the right mouse button is down

## createTimer

```javascript
var timer = client.createTimer()
```

Returns a [TimerUtil](../api/objects/timerutil.md) object.

## getAuraTarget

```javascript
var entity = client.getAuraTarget()
```

Returns an [EntityLivingBase](../api/objects/entitylivingbase.md) object that is the current target of the killaura. (Will be null if there is no current target)

## getClientColors

```javascript
var color = client.getClientColors()
```

Returns a [Pair ](broken-reference)of the `java.awt.Color` Object. It is the current client color based off the Client mod color setting.

```javascript
var colors = client.getClientColors()
var color1 = colors.getFirst()
var color2 = colors.getSecond()
```

## printClientMsg

```javascript
client.printClientMsg("This is a message")
```

This will print a message in the chat with the Tenacity text.

| Parameter | Type   | Description              |
| --------- | ------ | ------------------------ |
| text      | String | The text to be displayed |

## fps

```javascript
client.fps()
```

Returns the current fps as a **Number**.

## getIRCUsernameMap

```javascript
var ircMap = client.getIRCUsernameMap()
```

Returns a `java.util.HashMap` map. The key value pairs are Minecraft IGN to IRC username.

## getModule

```javascript
var killaura = client.getModule("kiLlAuRa")
var keystrokes = client.getModule("Keystrokes")
```

Returns a [Module ](../api/objects/module.md)object
