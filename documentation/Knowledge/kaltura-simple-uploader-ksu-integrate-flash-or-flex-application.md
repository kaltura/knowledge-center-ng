---
layout: page
title: "Kaltura Simple Uploader (KSU) - Integrate in a Flash or Flex Application"
date: 2012-03-27 00:22:10
---

<p class="mce-procedure">
  To integrate the Kaltura Simple Uploader (KSU) in a Flash or Flex application
</p>

1.  Edit KUpload.as. Remove the following line from the init() function:  
    addEventListener([Event][1].ADDED\_TO\_STAGE, addedToStageHandler);
2.  Create an init object with the same parameters that KUploader gets from flashVars when using HTML + Javascript mode.
3.  Add the following init function. Call the function and pass the init object you created.  
    public function initKUploader (initParams:[Object][2]):void  
    {  
            var initCommand:InitCommand = new InitCommand(initParams);  
            initCommand.execute();  
    }
4.  Create your UI in Flash/Flex.
5.  On your upload button MOUSE_EVENT.CLICK listener, call the browse(); method of KUploader.
6.  For the rest of the events to work in your Flash/Flex application, edit NotifyShellCommand.as. Replace the contents of the execute() function with code to dispatch the events to your application instead of calling ExternalInterface.

 [1]: http://www.google.com/search?q=event%20inurl:http://livedocs.adobe.com/flex/201/langref/%20inurl:event.html&filter=0&num=100&btnI=lucky
 [2]: http://www.google.com/search?q=object%20inurl:http://livedocs.adobe.com/flex/201/langref/%20inurl:object.html&filter=0&num=100&btnI=lucky

After completing the upload flow, retain the IDs of the entries that were added, and call the getentry API (using the [flash/flex client library][3]) to retrieve the new entry that was created.  
You can also modify various parameters before upload using the KUploader APIs. See [Kaltura Simple Uploader (KSU) - Website Integration Guide][4] for a complete list of methods and parameters.

 [3]: http://www.kaltura.com/api_v3/testme/client-libs.php
 [4]: http://knowledge.kaltura.com/kaltura-simple-uploader-ksu-website-integration-guide

## Important Security Note

Due to security restrictions in Flash Player v10, any browse operation must be triggered as a result of user interaction. Therefore, a user must click the swf itself to show the file dialogue box.  
To overcome this security restriction, Kaltura recommends not using the browse() API function. Instead, place the swf above the real GUI that the user interacts with so that the actual "click" event is triggered from the KUploader flash.

## Errors – Flash Player Exceptions

*   Limitations error – "Cannot upload, limitations exceeded. Please check for errors"  
    Thrown if the upload() function is invoked while an error exists.
*   Upload error - "Cannot add entries, some uploads failed. Either re-upload or remove the files"  
    Thrown if the addEntries() function is invoked while an error exists.

The error can be polled by calling getError();

### For Further Information

To learn more about KSU APIs and usage, see [Kaltura Simple Uploader (KSU) - Website Integration Guide][4].

[Learn more about the KSU][5].

 [5]: http://knowledge.kaltura.com/search/KSU