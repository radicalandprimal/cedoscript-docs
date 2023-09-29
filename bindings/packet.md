---
description: Information about the packet binding
---

# Packet

{% hint style="info" %}
These fields reference ids not the actually packet class

See [player.sendPacket(](player.md#sendpacket) for the use-cases of these packets

or [event.getPacket().getID()](../api/events.md#packet-send)
{% endhint %}

## Functions

### newPlayerCapabilities

```javascript
var capabilities = packet.newPlayerCapabilities()
```

Returns a new [PlayerAbilities ](../api/objects/player-abilities.md)object

## Client Packets

### C00Handshake

```
packet.C00Handshake
```

### C00PacketLoginStart

```
packet.C00PacketLoginStart
```

### C00PacketServerQuery

```
packet.C00PacketServerQuery
```

### C0DPacketCloseWindow

```
packet.C0DPacketCloseWindow
```

### C0EPacketClickWindow

```
packet.C0EPacketClickWindow
```

### C0BPacketEntityAction

```
packet.C0BPacketEntityAction
```

### C0APacketAnimation

```
packet.C0APacketAnimation
```

### C0CPacketInput

```
packet.C0CPacketInput
```

### C0CPacketInput

```
packet.C0CPacketInput
```

### C0FPacketConfirmTransaction

```
packet.C0FPacketConfirmTransaction
```

### C00PacketKeepAlive

```
packet.C00PacketKeepAlive
```

### C01PacketPing

```
packet.C01PacketPing
```

### C01PacketChatMessage

```
packet.C01PacketChatMessage
```

### C02PacketUseEntity

```
packet.C02PacketUseEntity
```

### C02PacketUseEntity

```
packet.C02PacketUseEntity
```

### C03PacketPlayer

```
packet.C03PacketPlayer
```

### C04PacketPlayerPosition

```
packet.C04PacketPlayerPosition
```

### C05PacketPlayerLook

```
packet.C05PacketPlayerLook
```

### C06PacketPlayerPosLook

```
packet.C06PacketPlayerPosLook
```

### C07PacketPlayerDigging

```
packet.C07PacketPlayerDigging
```

### C08PacketPlayerBlockPlacement

```
packet.C08PacketPlayerBlockPlacement
```

### C09PacketHeldItemChange

```
packet.C09PacketHeldItemChange
```

### C13PacketPlayerAbilities

```
packet.C13PacketPlayerAbilities
```

### C14PacketTabComplete

```
packet.C14PacketTabComplete
```

### C15PacketClientSettings

```
packet.C15PacketClientSettings
```

### C16PacketClientStatus

```
packet.C16PacketClientStatus
```

### C17PacketCustomPayload

```
packet.C17PacketCustomPayload
```

### C18PacketSpectate

```
packet.C18PacketSpectate
```

### C19PacketResourcePackStatus

```
packet.C19PacketResourcePackStatus
```

## Server Packets

### S00PacketKeepAlive

```
packet.S00PacketKeepAlive
```

### S2DPacketOpenWindow

```
packet.S2DPacketOpenWindow
```

### S2EPacketCloseWindow

```
packet.S2EPacketCloseWindow
```

### S2FPacketSetSlot

```
packet.S2FPacketSetSlot
```

### S3FPAcketCustomPayload

```
packet.S3FPacketCustomPayload
```

### S08PacketPlayerPosLook

```
packet.S08PacketPlayerPosLook
```

### S09PacketHeldItemChange

```
packet.S09PacketHeldItemChange
```

### S12PacketEntityVelocity

```
packet.S12PacketEntityVelocity
```

### S27PacketExplosion

```
packet.S27PacketExplosion
```

### S32PacketConfirmTransaction

```
packet.S32PacketConfirmTransaction
```
