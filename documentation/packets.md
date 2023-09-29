---
description: Information about how packets should be used and sent.
---

# Packets

{% hint style="info" %}
Packets listed on here are the only ones that are able to be sent with [player.sendPacket](../bindings/player.md#sendpacket)\
For more documentation about packets not listed here please visit [this link](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Serverbound\_2)
{% endhint %}

### **Confirm Transaction**

```java
player.sendPacket(packet.C0FPacketConfirmTransaction, windowID, actionNumber, accepted)
```

If a transaction sent by the client was not accepted, the server will reply with a [Confirm Transaction](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Confirm\_Transaction) ([Play](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Play), 0x32, clientbound) packet with the Accepted field set to false. When this happens, the client must reflect the packet to apologize (as with movement), otherwise the server ignores any successive transactions.

| Field        | Type    | Description                                                                                    |
| ------------ | ------- | ---------------------------------------------------------------------------------------------- |
| windowID     | Number  | The ID of the window the action occurred in                                                    |
| actionNumber | Number  | Every action that is to be accepted has a unique number. This field corresponds to that number |
| accepted     | Boolean | Whether the action was accepted                                                                |

### Keepalive Packet

```javascript
player.sendPacket(packet.C00PacketKeepAlive, id)
```

The server will frequently send out a keep-alive, each containing a random ID. The client must respond with the same packet.

| Field | Type   | Description                   |
| ----- | ------ | ----------------------------- |
| id    | Number | The random ID mentioned above |

### Player&#x20;

```javascript
player.sendPacket(packet.C03PacketPlayer, ground)
```

This packet as well as [Player Position](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Player\_Position) ([Play](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Play), 0x04, serverbound), [Player Look](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Player\_Look) ([Play](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Play), 0x05, serverbound), and [Player Position And Look](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Player\_Position\_And\_Look\_2) ([Play](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Play), 0x06, serverbound) are called the “serverbound movement packets”. At least one of them must be sent on each tick to ensure that servers will update things like player health correctly. Vanilla clients will send Player Position once every 20 ticks even for a stationary player, and Player on every other tick.

This packet is used to indicate whether the player is on ground (walking/swimming), or airborne (jumping/falling).

When dropping from sufficient height, fall damage is applied when this state goes from false to true. The amount of damage applied is based on the point where it last changed from true to false. Note that there are several movement related packets containing this state.

| Field  | Type    | Description                                          |
| ------ | ------- | ---------------------------------------------------- |
| ground | Boolean | True if the client is on the ground, false otherwise |

### Player Position

```javascript
player.sendPacket(packet.C04PacketPlayerPosition, x, y, z, ground) 
```

Updates the player's XYZ position on the server.

If the distance between the last known position of the player on the server and the new position set by this packet is greater than 100 units, this will result in the client being kicked for “You moved too quickly :( (Hacking?)”

If the distance is greater than 10 units, the server will log the warning message "\<name> moved too quickly!", followed by two coordinate triples (maybe movement delta?), but will not kick the client.

Also if the fixed-point number of X or Z is set greater than 3.2×107 the client will be kicked for “Illegal position”.

| Field  | Type    | Description                                          |
| ------ | ------- | ---------------------------------------------------- |
| x      | Number  | Absolute position                                    |
| y      | Number  | Absolute position, normally Head Y - 1.62            |
| z      | Number  | Absolute position                                    |
| ground | Boolean | True if the client is on the ground, false otherwise |

### Player Look

```javascript
player.sendPacket(packet.C05PacketPlayerLook, yaw, pitch, ground)
```

Updates the direction the player is looking in.

Yaw is measured in degrees, and does not follow classical trigonometry rules. The unit circle of yaw on the XZ-plane starts at (0, 1) and turns counterclockwise, with 90 at (-1, 0), 180 at (0,-1) and 270 at (1, 0). Additionally, yaw is not clamped to between 0 and 360 degrees; any number is valid, including negative numbers and numbers greater than 360.

Pitch is measured in degrees, where 0 is looking straight ahead, -90 is looking straight up, and 90 is looking straight down.

| Field  | Type    | Description                                          |
| ------ | ------- | ---------------------------------------------------- |
| yaw    | Number  | Absolute rotation on the X Axis, in degrees          |
| pitch  | Number  | Absolute rotation on the Y Axis, in degrees          |
| ground | Boolean | True if the client is on the ground, false otherwise |

### **Player Position And Look**

```javascript
player.sendPacket(packet.C06PacketPlayerPosLook, x, y, z, yaw, pitch, ground)
```

A combination of [Player Look](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Player\_Look) and [Player Position](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Player\_Position).

| Field  | Type    | Description                                          |
| ------ | ------- | ---------------------------------------------------- |
| x      | Number  | Absolute position                                    |
| y      | Number  | Absolute position, normally Head Y - 1.62            |
| z      | Number  | Absolute position                                    |
| yaw    | Number  | Absolute rotation on the X Axis, in degrees          |
| pitch  | Number  | Absolute rotation on the Y Axis, in degrees          |
| ground | Boolean | True if the client is on the ground, false otherwise |

### Player Digging

```javascript
player.sendPacket(packet.C07PacketPlayerDigging, status, x, y, z, facing)
```

Sent when the player mines a block. A Notchian server only accepts digging packets with coordinates within a 6-unit radius of the player's position.

| Field  | Type                                           | Description                                       |
| ------ | ---------------------------------------------- | ------------------------------------------------- |
| status | [C07 Action](../bindings/action.md#c07-action) | The action the player is taking against the block |
| x      | Number                                         | Pos x of the action                               |
| y      | Number                                         | Pos y of the action                               |
| z      | Number                                         | Pos z of the action                               |
| facing | [Facing](../bindings/facing.md)                | The face being hit                                |

### **Player Block Placement**

```java
player.sendPacket(packet.C08PacketPlayerBlockPlacement, x, y, z, 
    playedBlockDirection, itemStack, facingX, facingY, facingZ)
```

In normal operation (i.e. placing a block), this packet is sent once, with the values set normally.

This packet has a special case where X, Y, Z, and Face are all -1. (Note that Y is unsigned so set to 255.) This special packet indicates that the currently held item for the player should have its state updated such as eating food, pulling back bows, using buckets, etc.

In a Notchian Beta client, the block or item ID corresponds to whatever the client is currently holding, and the client sends one of these packets any time a right-click is issued on a surface, so no assumptions can be made about the safety of the ID. However, with the implementation of server-side inventory, a Notchian server seems to ignore the item ID, instead operating on server-side inventory information and holding selection. The client has been observed (1.2.5 and 1.3.2) to send both real item IDs and -1 in a single session.

Special note on using buckets: When using buckets, the Notchian client might send two packets: first a normal and then a special case. The first normal packet is sent when you're looking at a block (e.g. the water you want to scoop up). This normal packet does not appear to do anything with a Notchian server. The second, special case packet appears to perform the action — based on current position/orientation and with a distance check — it appears that buckets can only be used within a radius of 6 units.

| Field                | Type                                     | Description                                       |
| -------------------- | ---------------------------------------- | ------------------------------------------------- |
| x                    | Number                                   | Block position X                                  |
| y                    | Number                                   | Block position Y                                  |
| z                    | Number                                   | Block position Z                                  |
| playedBlockDirection | Number                                   | The face on which the block is placed (see above) |
| itemStack            | [ItemStack](../api/objects/itemstack.md) | Item being used                                   |
| facingX              | Number                                   | The X position of the crosshair on the block      |
| facingY              | Number                                   | The Y position of the crosshair on the block      |
| facingZ              | Number                                   | The Z position of the crosshair on the block      |

### Held Item Change

```javascript
player.sendPacket(packet.C09PacketHeldItemChange, slot)
```

Sent when the player changes the slot selection

| Field | Type   | Description                                  |
| ----- | ------ | -------------------------------------------- |
| slot  | Number | The slot which the player has selected (0–8) |

### Animation

```javascript
player.sendPacket(packet.C0APacketAnimation)
```

Sent when the player's arm swings

### Entity Action

```javascript
player.sendPacket(packet.C0BPacketEntityAction, action)
```

Sent by the client to indicate that it has performed certain actions: sneaking (crouching), sprinting, exiting a bed, jumping with a horse, and opening a horse's inventory while riding it.

{% hint style="info" %}
We default the Entity parameter in C0Bs as You/thePlayer
{% endhint %}

| Field  | Type                                           | Description                     |
| ------ | ---------------------------------------------- | ------------------------------- |
| action | [C0B Action](../bindings/action.md#c0b-action) | Action to perform on the player |

### Steer Vehicle

```javascript
player.sendPacket(packet.C0CPacketInput, strafeSpeed, forwardSpeed, 
    jumping, sneaking)
```

When you are riding an entity or vehicle, these will be sent in replacement of movement packets.

| Field        | Type    | Description                              |
| ------------ | ------- | ---------------------------------------- |
| strafeSpeed  | Number  | The speed you are strafing at            |
| forwardSpeed | Number  | The speed in which you are going forward |
| jumping      | Boolean | True if you are jumping                  |
| sneaking     | Boolean | True if you are sneaking                 |

### Close Window

```javascript
player.sendPacket(packet.C0DPacketCloseWindow, windowID) 
```

This packet is sent by the client when closing a window.

Notchian clients send a Close Window packet with Window ID 0 to close their inventory even though there is never an [Open Window](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Open\_Window) packet for the inventory.

| Field    | Type   | Description              |
| -------- | ------ | ------------------------ |
| windowID | Number | The ID of the gui window |

### Use Entity

```javascript
player.sendPacket(packet.C02PacketUseEntity, entity, action) 
```

This packet is sent from the client to the server when the client attacks or right-clicks another entity (a player, minecart, etc).

A Notchian server only accepts this packet if the entity being attacked/used is visible without obstruction and within a 4-unit radius of the player's position.

Note that middle-click in creative mode is interpreted by the client and sent as a [Creative Inventory Action](https://wiki.vg/index.php?title=Protocol\&oldid=7368#Creative\_Inventory\_Action) packet instead.

| Field  | Type                                                          | Description                  |
| ------ | ------------------------------------------------------------- | ---------------------------- |
| entity | Entity/[EntityLivingBase](../api/objects/entitylivingbase.md) | Entity to take the action on |
| action | [C02 Action](../bindings/action.md#c02-action)                | The action to be taken       |

### Player Abilities

```javascript
player.sendPacket(packet.C13PacketPlayerAbilities, abilities) 
```

The vanilla client sends this packet when the player starts/stops flying with the Flags parameter changed accordingly. All other parameters are ignored by the vanilla server.

| Field     | Type                                            | Description                 |
| --------- | ----------------------------------------------- | --------------------------- |
| abilities | [Player Abilities](packets.md#player-abilities) | The abilities of the player |

### Client Status

```javascript
player.sendPacket(packet.C16PacketClientStatus, state)
```

Sent when the client is ready to complete login and when the client is ready to respawn after death.

| Field | Type                                           | Description              |
| ----- | ---------------------------------------------- | ------------------------ |
| state | [C16 Status](../bindings/action.md#c16-status) | The status of the client |

### Spectate

```javascript
player.sendPacket(packet.C18PacketSpectate, uuid)
```

Teleports the player to the given entity. The player must be in spectator mode.

The Notchian client only uses this to teleport to players, but it appears to accept any type of entity. The entity does not need to be in the same dimension as the player; if necessary, the player will be respawned in the right world. If the given entity cannot be found (or isn't loaded), this packet will be ignored. It will also be ignored if the player attempts to teleport to themselves.

| Field | Type                                                                  | Description                           |
| ----- | --------------------------------------------------------------------- | ------------------------------------- |
| uuid  | [UUID](https://docs.oracle.com/javase/8/docs/api/java/util/UUID.html) | The UUID of the player to teleport to |
