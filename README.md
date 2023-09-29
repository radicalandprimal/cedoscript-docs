# Introduction

## Information

**cedoscript**: the way scripting was meant to be.\
\
cedoscript was built on the idea of being as clean as possible without uneccesary strings, parameters, and pseudocode that other scripting systems forced users to endure.

## Setting up

To setup a script for use you have to create a variable and assign it to the return of the function `initScript`

```javascript
var script = initScript({
    name: "Test Script",
    description: "This is the description",
    author: "cedo"
})
```

{% hint style="warning" %}
&#x20;You **must** declare name, description, and author variables.
{% endhint %}

#### Hooking an event

To hook an event we use the script variable then call one of the predefined functions for the specified event.

```javascript
var script = initScript({
    name: "Test Script",
    description: "This is the description",
    author: "cedo"
})

script.onRender3D(function (event) {
    print("This will print in the console on render 3D event")
})
```

{% hint style="warning" %}
You will **not** be able to upload your script to the cloud without an event hooked
{% endhint %}
