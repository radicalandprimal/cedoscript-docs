---
description: Information about the player binding
---

# Player

## sendPacket

```javascript
player.sendPacket(packetID, args...)
```

See [packet documentation](../documentation/packets.md)

## sendMessage

```javascript
player.sendMessage(msg)
```

| Parameter | Type   | Description                         |
| --------- | ------ | ----------------------------------- |
| msg       | String | Message you want the player to send |

## respawn

```javascript
player.respawn()
```

Sends a respawn packet

## swingItem

```javascript
player.swingItem()
```

Makes the player swing the current item.

## setPitch

```javascript
player.setPitch(pitch)
```

Sets the player's pitch

| Parameter | Type   | Description      |
| --------- | ------ | ---------------- |
| pitch     | Number | New player pitch |

## setYaw

```javascript
player.setYaw(yaw)
```

Sets the player's yaw

| Parameter | Type   | Description    |
| --------- | ------ | -------------- |
| yaw       | Number | New player yaw |

## setMotionX

```javascript
player.setMotionX(motionX)
```

Sets the player's motionX

| Parameter | Type   | Description        |
| --------- | ------ | ------------------ |
| motionX   | Number | New player motionX |

## setMotionY

```javascript
player.setMotionY(motionY)
```

Sets the player's motionY

| Parameter | Type   | Description        |
| --------- | ------ | ------------------ |
| motionY   | Number | New player motionY |

## setMotionZ

```javascript
player.setMotionZ(motionZ)
```

Sets the player's motionZ

| Parameter | Type   | Description        |
| --------- | ------ | ------------------ |
| motionZ   | Number | New player motionZ |

## setPosition

```javascript
player.setPosition(x, y, z)
```

Sets the players position

| Parameter | Type   | Description      |
| --------- | ------ | ---------------- |
| x         | Number | New player pos x |
| y         | Number | New player pos y |
| z         | Number | New player pos z |

## jump

```javascript
player.jump()
```

Makes the player jump

## timerSpeed

```javascript
var currentTimerSpeed = player.timerSpeed()
```

Returns the player's current timer speed as a **Number**

## speed

```javascript
var currentSpeed = player.speed()
```

Returns the player's current speed as a **Number**

## setSpeed

```javascript
player.setSpeed(speed)
```

Sets the player's speed

| Parameter | Type   | Description      |
| --------- | ------ | ---------------- |
| speed     | Number | New player speed |

## setSneaking

```javascript
player.setSneaking(sneaking)
```

Sets to true to make the player sneak

| Parameter | Type    | Description                          |
| --------- | ------- | ------------------------------------ |
| sneaking  | Boolean | Set to true to make the player sneak |

## setSprinting

```javascript
player.setSprinting(sprinting)
```

Sets to true to make the player sprint

| Parameter | Type    | Description                           |
| --------- | ------- | ------------------------------------- |
| sprinting | Boolean | Set to true to make the player sprint |

## setFallDistance

```javascript
player.setFallDistance(fallDistance)
```

Sets the player's fall distance

| Parameter    | Type   | Description              |
| ------------ | ------ | ------------------------ |
| fallDistance | Number | New player fall distance |

## leftClick

```javascript
player.leftClick()
```

Clicks the left mouse button

## rightClick

```javascript
player.rightClick()
```

Clicks the right mouse button

## setHeldItemSlot

```javascript
player.setHeldItemSlot(slot)
```

Set the current held item of the local player.

| Parameter | Type   | Description                              |
| --------- | ------ | ---------------------------------------- |
| slot      | Number | New slot of the item in the hotbar (0-8) |

## collidedHorizontally

```javascript
player.collidedHorizontally()
```

Returns true if the player was collided horizontally

## collidedVertically

```javascript
player.collidedVertically()
```

Returns true if the player was collided horizontally

## collided

```javascript
player.collided()
```

Returns true if the player was collided at all

## moving

```javascript
player.moving()
```

Returns true if the player is moving

## sneaking

```javascript
player.sneaking()
```

Returns true if the player is sneaking

## sprinting

```javascript
player.sprinting()
```

Returns true if the player is sprinting

## eating

```javascript
player.eating()
```

Returns true if the player is eating

## onGround

```javascript
player.onGround()
```

Returns true if the player is on ground

## airBorne

```javascript
player.airBorne()
```

Returns true if the player is air borne

## onLadder

```javascript
player.onLadder()
```

Returns true if the player is on a ladder

## inWater

```javascript
player.inWater()
```

Returns true if the player is in water

## inLava

```javascript
player.inLava()
```

Returns true if the player is in lava

## inWeb

```javascript
player.inWeb()
```

Returns true if the player is in a web

## inPortal

```javascript
player.inPortal()
```

Returns true if the player is in a portal

## usingItem

```javascript
player.usingItem()
```

Returns true if the player is using an item

## burning

```javascript
player.burning()
```

Returns true if the player is burning

## dead

```javascript
player.dead()
```

Returns true if the player is dead

## isPotionActive

```javascript
player.isPotionActive(potion)
```

| Parameter | Type                | Description                                     |
| --------- | ------------------- | ----------------------------------------------- |
| potion    | [Potion](potion.md) | Checks to see if the specified potion is active |

## name

```javascript
player.name()
```

Returns the player's name as a **String**

## hurtTime

```javascript
player.hurtTime()
```

Returns the player's hurt time as a **Number**

## **heldItemSlot**

```javascript
player.heldItemSlot()
```

Returns the player's currently held item's slot as a **Number**

## ticksExisted

```javascript
player.ticksExisted()
```

Returns the player's ticks existed as a **Number**

## fallDistance

```javascript
player.fallDistance()
```

Returns the player's fall distance as a **Number**

## health

```javascript
player.health()
```

Returns the player's health as a **Number**

## maxHealth

```javascript
player.maxHealth()
```

Returns the player's max health as a **Number**

## armor

```javascript
player.armorValue()
```

Returns the player's total armor value as a **Number**

## hunger

```javascript
player.hunger()
```

Returns the player's food level as a **Number**

## absorption

```javascript
player.absorption()
```

Returns the player's absorption level as a **Number**

## pitch

```javascript
player.pitch()
```

Returns the player's pitch as a **Number**

## **yaw**

```javascript
player.yaw()
```

Returns the player's yaw as a **Number**

## **x**

```javascript
player.x()
```

Returns the player's x pos as a **Number**

## y

```javascript
player.y()
```

Returns the player's y pos as a **Number**

## **z**

```javascript
player.z()
```

Returns the player's z pos as a **Number**

## **prevX**

```javascript
player.prevX()
```

Returns the player's previous x pos as a **Number**

## y

```javascript
player.prevY()
```

Returns the player's previous y pos as a **Number**

## **z**

```javascript
player.prevZ()
```

Returns the player's previous z pos as a **Number**

## **motionX**

```javascript
player.motionX()
```

Returns the player's motion x as a **Number**

## **motionY**

```javascript
player.motionY()
```

Returns the player's motion y as a **Number**

## **motionZ**

```javascript
player.motionZ()
```

Returns the player's motion z as a **Number**

## getBaseMoveSpeed

```javascript
player.getBaseMoveSpeed()
```

Returns the base move speed of the player as a **Number**

## getServerIP

```javascript
var serverIP = player.getServerIP()
```

Returns the current server ip as a **String**, returns "singleplayer" if the player is in singleplayer mode

## getInventorySlot

```javascript
var stack = player.getInventorySlot();
```

Returns an [ItemStack](../api/objects/itemstack.md) object of the specified slot in the player's inventory. Returns null if there is no stack in that slot
