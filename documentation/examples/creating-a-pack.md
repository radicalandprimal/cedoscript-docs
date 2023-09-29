# Creating a Pack

You can now load configs and download other scripts with the power of one script

## How to

To load either a script or config we will make use of the .load command in Tenacity

1. You will need to go to the config/script and hover over the "Hover for more information" text.
2. Click the text while holding the SHIFT key and the share code will be copied to your clipboard.
3. Go into your script and put the following psuedocode in your onEnable function.

```javascript
script.onEnable(function () {
    //This will be for loading a cloud config
    player.sendMessage(".load [share-code]")
    
    //This will be for downloading a cloud script
    player.sendMessage(".load [share-code]")
    
    //This makes sure that when we reload all scripts this script 
    //does not have to be reloaded
    script.overrideReload()
})
```

This will load a config and a cloud script\
Then since when loading a new script we have to reload all the scripts we override reloading for this specfic script
