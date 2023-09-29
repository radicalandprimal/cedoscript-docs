---
description: >-
  This is a timer utility that allows to keep track of time and run certain code
  on a specified interval
---

# TimerUtil

## Creation

```javascript
var timerUtil = client.createTimer()
```

Returns a [TimerUtil](timerutil.md) object.

## Functions

### getTime

```javascript
timerUtil.getTime()
```

Returns the current time of the timer as a **Number**

### reset

```javascript
timerUtil.reset()
```

This will reset the time elapsed

### hasTimeElapsed

```javascript
timerUtil.hasTimeElapsed(1000)

//or

timerUtil.hasTimeElapsed(1000, true)
```

Returns true if the timer has elapsed the specified time

| Parameter        | Type    | Description                                                                   |
| ---------------- | ------- | ----------------------------------------------------------------------------- |
| time             | Number  | The time elapsed to check in milliseconds                                     |
| reset (Optional) | Boolean | Set to true if you want to reset the time elapsed if the method returned true |
