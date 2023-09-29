---
description: This will display how you can simulate making a command
---

# Simulate a command

```javascript
var script = initScript({    
    name: "Clip Command",    
    description: "Use +clip [value] to vclip up and down",    
    author: "cedo"
})

script.onPlayerSendMessage(function (event) {    
    var message = event.getMessage()    
    if (message.contains("+clip")) {        
        event.cancel()        
        // Split it into an array by using spaces
        var array = message.split(" ")
        // if there is more than one message after the "-clip"       
        if (array.length > 1) {            
            var clipValue = parseInt(array[1])  
            // Check if it failed to parse the string          
            if (clipValue.isNaN()) {                
                client.printClientMsg("Invalid clip value " + array[1])            
            } else {
                //Finally set the position according to the clipvalue on the y axis                
                player.setPosition(player.x(), player.y() + clipValue, player.z())            
            }        
        } else {            
            client.printClientMsg("Error please specify a distance to clip")        
        }    
    }
})
```

<figure><img src="../../.gitbook/assets/Screenshot 2022-03-03 114951.png" alt=""><figcaption><p>Command is fully working and all edge cases are caught</p></figcaption></figure>
