---
description: >-
  This page will explain all the allowed imports from Java (Anything not on this
  list is not allowed to be imported)
---

# Java Imports

## How to import

```javascript
var Object = Java.type(package_name)
```

This code will import the java class and allow access to it's available methods

## Imports

### Keyboard

```javascript
var Keyboard = Java.type("org.lwjgl.input.Keyboard")
```

See this for full documentation: [https://legacy.lwjgl.org/javadoc/org/lwjgl/input/Keyboard.html](https://legacy.lwjgl.org/javadoc/org/lwjgl/input/Keyboard.html)

### Mouse

```javascript
var Mouse = Java.type("org.lwjgl.input.Mouse")
```

See this for full documentation: [https://legacy.lwjgl.org/javadoc/org/lwjgl/input/Mouse.html](https://legacy.lwjgl.org/javadoc/org/lwjgl/input/Mouse.html)

### GL11

```javascript
var GL11 = Java.type("org.lwjgl.opengl.GL11")
```

See this for full documentation: [https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL11.html](https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL11.html)

### GL13

```javascript
var GL13 = Java.type("org.lwjgl.opengl.GL13")
```

See this for full documentation: [https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL13.html](https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL13.html)

### GL14

```javascript
var GL14 = Java.type("org.lwjgl.opengl.GL14")
```

See this for full documentation: [https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL14.html](https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL14.html)

### GL20

```javascript
var GL20 = Java.type("org.lwjgl.opengl.GL20")
```

See this for full documentation: [https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL20.html](https://legacy.lwjgl.org/javadoc/org/lwjgl/opengl/GL20.html)

### Map

```javascript
var Map = Java.type("java.util.Map")
```

See this for full documentation: [https://docs.oracle.com/javase/8/docs/api/java/util/Map.html](https://docs.oracle.com/javase/8/docs/api/java/util/Map.html)

### HashMap

```javascript
var HashMap = Java.type("java.util.HashMap")
```

See this for full documentation: [https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html](https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html)

### List

```javascript
var List = Java.type("java.util.List")
```

See this for full documentation: [https://docs.oracle.com/javase/8/docs/api/java/util/List.html](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)

### ArrayList

```javascript
var ArrayList = Java.type("java.util.ArrayList")
```

See this for full documentation: [https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html)

### Math

```javascript
var Math = Java.type("java.lang.Math")
```

See this for full documentation: [https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html)

### Collectors

```javascript
var Collectors = Java.type("java.util.stream.Collectors")
```

See this for full documentation: [https://docs.oracle.com/javase/8/docs/api/java/util/stream/Collectors.html](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Collectors.html)

### Tuples

```javascript
var Pair = Java.type("dev.cedo.tuples.Pair")

var Triplet = Java.type("dev.cedo.tuples.Triplet")

var MutablePair = Java.type("dev.cedo.tuples.mutable.MutablePair")

var MutableTriplet = Java.type("dev.cedo.tuples.mutable.MutableTriplet")
```

See this for full documentation: [https://github.com/not-cedo/Tuples](https://github.com/not-cedo/Tuples) or the [Pair page](../api/objects/pair.md)
