---
description: Information about the world binding
---

# World

## setTimer

```javascript
world.setTimer(speed)
```

Sets the timer speed (Defualt timer speed is 1)

| Parameter | Type   | Description     |
| --------- | ------ | --------------- |
| speed     | Number | New timer speed |

## isSinglePlayer

```javascript
world.isSinglePlayer()
```

Returns true if the user is in a singleplayer world

## getLivingEntities

```javascript
world.getLivingEntities()
```

Returns a list of [EntityLivingBases](../api/objects/entitylivingbase.md). Refer to [this ](../api/objects/entitylivingbase.md#usage)to see how to loop through the entities.

## timer

```javascript
world.timer()
```

Returns the current timer speed as a **Number**
