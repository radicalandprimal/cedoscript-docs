# EntityLivingBase

## Usage

The only way to get an entity right now is through the following:

```javascript
var entity = client.getAuraTarget()
```

**Or**

```javascript
for (var i = 0; i <= (world.getLivingEntities().size() - 1); i++) {
        var entity = world.getLivingEntities().get(i)
        ...
        ...
}
```

## Functions

### getName

```javascript
var entityName = entity.getName()
```

This will return a **String** containing the entity's name

### getHealth

```javascript
var entityHealth = entity.getHealth()
```

This will return a **Number** with the entity's current health

### getMaxHealth

```javascript
var entityMaxHealth = entity.getMaxHealth()
```

This will return a **Number** with the entity's max health

### getPrevPosX

```javascript
var prevPosX = entity.getPrevPosX()
```

This will return a **Number** with the entity's previous position X value

### getPrevPosY

```javascript
var prevPosZ = entity.getPrevPosY()
```

This will return a **Number** with the entity's previous position Y value

### getPrevPosZ

```javascript
var prevPosZ = entity.getPrevPosZ()
```

This will return a **Number** with the entity's previous position Z value

### getPosX

```javascript
var posX = entity.getPosX()
```

This will return a **Number** with the entity's position X value

### getPosY

```javascript
var posY = entity.getPosY()
```

This will return a **Number** with the entity's position Y value

### getPosZ

```javascript
var posZ = entity.getPosZ()
```

This will return a **Number** with the entity's position Z value

### getMotionX

```javascript
var motionX = entity.getMotionX()
```

This will return a **Number** with the entity's motion X value

### getMotionY

```javascript
var motionY = entity.getMotionY()
```

This will return a **Number** with the entity's motion Y value

### getMotionZ

```javascript
var motionZ = entity.getMotionZ()
```

This will return a **Number** with the entity's motion Z value

### isOnGround

```javascript
var onGround = entity.isOnGround()
```

This will return **True** if the entity is on ground

### isCollidedHorizontally

```javascript
var onGround = entity.isCollidedHorizontally()
```

This will return **True** if the entity is is collided horizontally

### isCollidedVertically

```javascript
var onGround = entity.isCollidedVertically()
```

This will return **True** if the entity is is collided vertically

### isCollided

```javascript
var onGround = entity.isCollided()
```

This will return **True** if the entity is is collided

### isOnLadder

```javascript
var onLadder = entity.isOnLadder()
```

This will return **True** if the entity is is on a ladder

### getTotalArmorValue

```javascript
var armorValue = entity.getTotalArmorValue()
```

Gets the total value of the armor the entity currently has on

### getHeldItem

```javascript
var heldItem = entity.getHeldItem()
```

Returns an [ItemStack](itemstack.md) object of the entity's currently held item

### getHurtTime

```javascript
var hurtTime = entity.getHurtTime()
```

This will return a **Number** counting down from 10 when an entity is damaged

### getEquipmentInSlot

```javascript
var equipment = entity.getEquipmentInSlot(4)
```

Returns an [ItemStack](itemstack.md)

| Name | Type   | Description                 |
| ---- | ------ | --------------------------- |
| slot | Number | 0: Tool in Hand; 1-4: Armor |

### getRotationYawHead

```javascript
var yawHead = entity.getRotationYawHead();
```

Returns the yaw of the entity's head as a **Number**

### getRotation**Pitch**Head

```javascript
var pitchHead = entity.getRotationPitchHead();
```

Returns the pitch of the entity's head as a **Number**

### getAbsorptionAmount

```javascript
var yawHead = entity.getAbsorptionAmount();
```

Returns the absorption amount of the entity as a **Number**

### getUUID

```javascript
var uuid = entity.getUUID();
```

Returns a [UUID ](https://docs.oracle.com/javase/8/docs/api/java/util/UUID.html)object. Returns null if UUID does not exist or cannot be found.

{% hint style="danger" %}
This will not work if the entity is not a Player. i.e a mob or animal
{% endhint %}

### isMob

```javascript
var mob = entity.isMob();
```

Returns True if the entity is a mob

### isAnimal

```javascript
var animal = entity.isAnimal();
```

Returns True if the entity is an animal
