---
description: This allows interface with our Statistics modules
---

# Stats

{% hint style="warning" %}
The kill count, death count, and games played is only configured for Hypixel
{% endhint %}

{% hint style="info" %}
We would greatly appreciate if someone could make a statistics script working for almost every server
{% endhint %}

## Functions

### getKills

```javascript
var killCount = stats.getKills()
```

Returns a Number of the amount of kills you have

### getDeaths

```javascript
var deathCount = stats.getDeaths()
```

Returns a Number of your death count

### getKD

```javascript
var KDRatio = stats.getKD()
```

Returns a Number of your kill to death ratio

### getGamesPlayed

```javascript
var gamesPlayed = stats.getGamesPlayed()
```

Returns a Number with how many games you have played

### getPlayTime

```javascript
var playtime = stats.getPlayTime()
```

Returns an int array so that the first value "`playtime[0]`" will be the hours, "`playtime[1]`" will be minutes, and "`playtime[2]`" will be seconds
