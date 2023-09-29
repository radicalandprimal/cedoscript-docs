---
description: For usage in C13PlayerAbilities packet
---

# Player Abilities

## How to create

```javascript
var abilities = packet.newPlayerCapabilities()
```

## Functions

### disableDamage

```javascript
abilities.disableDamage = true
```

### isFlying

```javascript
abilities.isFlying = true
```

### allowFlying

```javascript
abilities.allowFlying = true
```

### isCreativeMode

```javascript
abilities.isCreativeMode = true
```

### allowEdit

```javascript
abilities.allowEdit = true
```

### getFlySpeed

```javascript
var speed = abilities.getFlySpeed()
```

### setFlySpeed

```javascript
abilities.setFlySpeed(2)
```

### getWalkSpeed

```javascript
var speed = abilities.getWalkSpeed()
```

### setPlayerWalkSpeed

```javascript
abilities.setPlayerWalkSpeed(2)
```
