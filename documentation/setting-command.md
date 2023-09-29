---
description: >-
  This will show how to use some of the commands Tenacity has to your advantage
  when scripting
---

# Setting Command

![](<../.gitbook/assets/image (8).png>)For the setting command there is a lot of different options and rules to follow

## How to use the setting command

To use the setting command you must do `.setting module_name setting_name value`

If there is spaces between the module name or setting name then you must use under scores for these spaces.

{% hint style="info" %}
Names are not case-sensitive
{% endhint %}

## How to turn off success messages

For those of you using scripting to modify an existing module on Tenacity then you may edit a setting many times over. This would normally spam your chat with messages saying that you successfully set the setting value. Well we have a solution for this.

To stop all of these messages from coming through just end every .setting command with the following text: `sendSuccess=false`

![This command will not send a message back saying that it successfully set the setting](<../.gitbook/assets/image (3).png>)

## Examples

### Mode Setting

![This changes the watermark mode in the HUD module to Tenacity mode](<../.gitbook/assets/image (8).png>)

### Boolean Setting

![This changes the custom font setting in the HUD module to false](<../.gitbook/assets/image (2).png>)

### Number Setting

![This changes the radius setting in Glow ESP to 4](../.gitbook/assets/image.png)

{% hint style="warning" %}
All values will be clamped to be within the specified increment of the setting

i.e. If you typed <mark style="color:red;">`.setting glowesp radius 3`</mark> then it would set the value to 2 because the setting increments by 2
{% endhint %}

### String Setting

![This would change the Client Name setting in HUD module to "cedoscript testing enterprises"](<../.gitbook/assets/image (7).png>)

{% hint style="info" %}
For a String Setting underscores are not needed for the value
{% endhint %}

### Multi Boolean Setting

![This would change the White Info option in the Info Options setting to true](<../.gitbook/assets/image (5).png>)

### Color Setting

![This would set the Animal Color in glow esp to red](<../.gitbook/assets/image (1).png>)

{% hint style="warning" %}
Alpha values are not supported. You must input a valid hex value.&#x20;
{% endhint %}
