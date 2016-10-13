---
layout: page
title: "Kaltura Simple Uploader (KSU) - Website Integration Guide"
date: 2012-03-27 00:34:09
---

The Kaltura Simple Uploader (KSU) is a standalone transparent widget. It enables content administrators and/or end users to upload media files by using a simple desktop browser selection. [Read a more detailed overview of the KSU widget][1].

 [1]: http://knowledge.kaltura.com/kaltura-simple-uploader-ksu

The KSU widget supports a variety of media upload workflows. The way you integrate this widget depends on the site-specific upload workflow you wish to implement.  
The generic Kaltura upload workflow consists of the following steps:

1.  End-user selects media file/s to be uploaded.
2.  Media file is uploaded to Kaltura system.
3.  (Optional) End-user sets metadata (tags, title etc.) for the uploaded media file/s. 
4.  An entry is created for the uploaded media file on the Kaltura server.

The KSU widget exposes interfaces, so each workflow step can be executed separately from within JavaScript methods. It is also possible to combine steps 2 and 4 if your workflow does not require any end-user interaction for metadata settings.  
Integrating the KSU widget into your web site requires that you add the following to your web page:

*   <a href="http://cdnknowledge.kaltura.com//sites/default/files/ksu_apiv3_integration_sample.zip" target="_blank"><strong><img src="http://cdnknowledge.kaltura.com//sites/default/files/Zip%20Archive%20Icon.png" width="24" height="21" style="margin: 0px !important;" />Download KSU Integration script.</strong></a>
*   [Include external scripts and supporting styles][2]
*   [JavaScript handler methods to react to upload events][3]
*   [JavaScript callback methods to activate Kaltura services via the KSU widget][4]
*   [Construct Kaltura objects for session initiation and populate variables to be passed to the embedded flash object][5].
*   [Set the location for the transparent KSU widget and for embedding the flash object][6].
*   [(Optional) Interactive form fields for dynamic user input][7] 

 [2]: #IncludeExternalScripts
 [3]: #ImplementJavaScriptHandlerMethods
 [4]: #ImplementCallbackMethods
 [5]: #ConstructKalturaObjects
 [6]: #SettheLocation
 [7]: #OptionalImplementInputFields

## Important Security Note

Due to security restrictions in Flash Player v10, any browse operation must be triggered as a result of user-interaction. Therefore, a user must click the swf itself to show the file dialogue box.  
To overcome this security restriction, Kaltura recommends not using the browse() API function. Instead, place the swf above the real GUI that the user interacts with so that the actual "click" event is triggered from the KUploader flash.

## Full Example Script

The following PHP/JavaScript script example demonstrates the integration of the KSU widget in a PHP based web application.

To run this script, please make sure you set your partner identifiers at the KALTURA\_PARTNER\_ID and KALTURA\_PARTNER\_SERVICE\_WEB\_SECRET constants.  
Look for detailed information on this example in the following sections.

<p class="mce-note-graphic">
  Console logs calls in this example script may assist understanding the script flow. This applies when using the Firebug extension for the Mozilla Firefox browser.
</p>

** **

## <a name="IncludeExternalScripts"></a>Include External Scripts and Supporting Styles

The following example includes external scripts that are required for the KSU widget implementation.

<pre class="brush: jscript;fontsize: 100; first-line: 1; ">&lt;html&gt;
&lt;head&gt;
&lt;!--include external scripts--&gt;
&lt;?php require_once("KalturaClient.php"); ?&gt;
&lt;script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/swfobject/2.2/swfobject.js"&gt;&lt;/script&gt;

&lt;!---set style to enable widget overlap --&gt;
&lt;style&gt;
        body { margin: 0px; overflow:hidden }
        #flashContainer{ position:relative; }
                #flashContainer span{ color:#333; font-size:16px; }
                object, embed{ position:absolute; top:0; left:0; z-index:999;}
&lt;/style&gt;</pre>

The KalturaClient.php scripts are part of the PHP Kaltura API Client Library,  included to enable the use of Kaltura objects.  
The swfobject.js script is the Google-hosted SWFObject script, used for embedding the KSU widget as a flash object.

A special style is defined within the example to enable the overlapping of the transparent KSU widget on top of the relevant GUI element to allow flash widget activation. Look for more information on this feature in the "Set the location of the transparent KSU widget and embed flash object" section.

## <a name="ImplementJavaScriptHandlerMethods"></a>Implement JavaScript Handler Methods to React to Upload Events

In the following example, the flashObj variable points to the KSU flash application, which enables external control of the widget’s functionality.   
The delegate array holds JavaScript handler methods that allow web applications to implement their workflow upon notification of media upload events arriving from the Kaltura servers.

<div>
  <div>
    <pre class="brush: jscript;fontsize: 100; first-line: 1; ">&lt;script language="JavaScript" type="text/javascript"&gt;
var flashObj;
var delegate = {};
 

//KSU handlers
delegate.readyHandler = function()
{
        flashObj = document.getElementById("uploader");
}

delegate.selectHandler = function()
{
        console.log("selectHandler()");
        console.log(flashObj.getTotalSize());
}

delegate.singleUploadCompleteHandler = function(args)
{
        console.log("singleUploadCompleteHandler", args[0].title);
}

delegate.allUploadsCompleteHandler = function()
{
        console.log("allUploadsCompleteHandler");
}

delegate.entriesAddedHandler = function(entries)
{
        console.log(entries[0].entryId)
}

delegate.progressHandler = function(args)
{
        console.log(args[2].title + ": " + args[0] + " / " + args[1]);
}

delegate.uiConfErrorHandler = function()
{
        console.log("ui conf loading error");
}</pre>
  </div>
  
  <div>
     The following lists the handler events and their applicative meaning.
  </div>
</div>

<table align="left">
  <thead>
    <tr>
      <th>
        Callback ID
      </th>
      
      <th>
        Description
      </th>
      
      <th>
        Parameters
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr align="left">
      <td style="text-align: left;">
        delegate.readyHandler
      </td>
      
      <td style="text-align: left;">
        The readyHandler method is activated upon server notification of successful load of the KSU widget. This event signals to the web application that the flash object is ready to interact with the JavaScript handler methods. The implementation of this method must include an initiation of the flashObj object.
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        delegate.selectHandler
      </td>
      
      <td style="text-align: left;">
        The selectHandler method is activated upon server notification of successful selection of media file/s to be uploaded. Web-applications may want to use this handler to inform end-users of the event.
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        delegate.singleUploadCompleteHandler
      </td>
      
      <td style="text-align: left;">
        The singleUploadCompleteHandler method is activated upon server notification of successful upload of one selected media file. It passes a single item array of entry objects, holding information on the uploaded file. Arg[0].title may be in use by a web application wishing to use this handler to inform end-users of the event.
      </td>
      
      <td style="text-align: left;">
        Arg = Array of single entry object
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        delegate.allUploadsCompleteHandler
      </td>
      
      <td style="text-align: left;">
        The allUploadsCompleteHandler method is activated upon server notification of successful upload of all media files selected within one session. A web application may want to use this handler to inform end-users of the event.
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        delegate.entriesAddedHandler
      </td>
      
      <td style="text-align: left;">
        The entriesAddedHandler method is activated upon server notification of successful entry creation for all media files selected in one session. It passes an array of Kaltura entry objects as an argument. entries[i].title may be used by a web application wishing to use this handler to inform end-users of the event.
      </td>
      
      <td align="left">
        <p style="text-align: left;">
          <span style="text-align: left;"><span><span>entries = Array  of entry </span> objects</span></span>
        </p>
        
        <ul>
          <li style="text-align: left;">
            entries[i].title
          </li>
          <li style="text-align: left;">
            entries[i].entryID
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        delegate.progressHandler
      </td>
      
      <td style="text-align: left;">
        The progressHandler method enables web applications to implement a progress bar, informing users of the progress of long uploads based on notification from Kaltura servers.
      </td>
      
      <td style="text-align: left;">
        <span style="text-align: left;">Arg = Array</span> <ul>
          <li style="text-align: left;">
            Arg[0] = number of bytes already loaded
          </li>
          <li style="text-align: left;">
            Arg[1] = total number of bytes to upload
          </li>
          <li style="text-align: left;">
            Arg[2] = Kaltura entry object containing information on the uploaded media file.
          </li>
          <li style="text-align: left;">
            Arg[2].title holds info on media name
          </li>
        </ul>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        delegate.uiConfErrorHandler
      </td>
      
      <td style="text-align: left;">
        This uiConfErrorHandler method is activated upon server notification of failure in uploading the KSU widget configuration XML
      </td>
      
      <td style="text-align: left;">
        N/A 
      </td>
    </tr>
  </tbody>
</table>

## <a name="ImplementCallbackMethods"></a>Implement Callback Methods to Activate Kaltura Services via the KSU Widget

In the following example, JavaScript callback methods are implemented to activate Kaltura services upon application workflow or end-user actions. Kaltura services are activated by calling public methods of the KSU widget.

<div>
  <div>
    <pre class="brush: jscript;fontsize: 100; first-line: 1; ">//KUplaoder callbacks  
function upload()
{
        flashObj.upload();
}
 

function setTags(tags, startIndex, endIndex)
{
        flashObj.setTags(tags, startIndex, endIndex);
}

function addTags(tags, startIndex, endIndex)
{
        flashObj.addTags(tags, startIndex, endIndex);
}
function setTitle(title, startIndex, endIndex)
{
        flashObj.setTitle(title, startIndex, endIndex);
}

function getFiles()
{
        var files = flashObj.getFiles();
        console.log(files[0].title);
}

function addEntries()
{
        flashObj.addEntries();
}

function stopUploads()
{
        flashObj.stopUploads();
}

function setMaxUploads(value)
{
        flashObj.setMaxUploads(value);
}

function setPartnerData(value)
{
        flashObj.setPartnerData(value);
}

function setMediaType()
{
        var mediaType = mediaTypeInput.value;
        console.log(mediaType);
        flashObj.setMediaType(mediaType);
}

function addTagsFromForm()
{
        var tags = document.getElementById("tagsInput").value.split(",");
        var startIndex = parseInt(tagsStartIndex.value);
        var endIndex = parseInt(tagsEndIndex.value);
        addTags(tags, startIndex, endIndex);
}

function setTitleFromForm()
{
        var startIndex = parseInt(titleStartIndex.value);
        var endIndex = parseInt(titleEndIndex.value);
        setTitle(titleInput.value, startIndex, endIndex);
}

function removeFilesFromForm()
{
        var startIndex = parseInt(removeStartIndex.value);
        var endIndex = parseInt(removeEndIndex.value);
        flashObj.removeFiles(startIndex, endIndex)
        console.log(flashObj.getTotalSize());
}

function setGroupId(value)
{
        flashObj.setGroupId(value);
}

function setPermissions(value)
{
        flashObj.setPermissions(value);
}

function setSiteUrl(value)
{
        flashObj.setSiteUrl(value);
}

function setScreenName(value)
{
        flashObj.setScreenName(value);
}

//set parameters to be taken from user input field
var tagsInput;
var tagsStartIndex;
var tagsEndIndex;

var titleInput;
var titleStartIndex;
var titleEndIndex;

var removeStartIndex;
var removeEndIndex;
var maxUploadsInput;

var partnerDataInput;
var mediaTypeInput
var groupId;
var permissions;
var screenName;
var siteUrl;

function onLoadHandler()
{
        tagsInput = document.getElementById("tagsInput");
        tagsStartIndex = document.getElementById("tagsStartIndex");
        tagsEndIndex = document.getElementById("tagsEndIndex");

        titleInput = document.getElementById("titleInput");
        titleStartIndex = document.getElementById("titleStartIndex");
        titleEndIndex = document.getElementById("titleEndIndex");

        removeStartIndex = document.getElementById("removeStartIndex");;
        removeEndIndex = document.getElementById("removeEndIndex");

        maxUploadsInput = document.getElementById("maxUploadsInput");
        partnerDataInput = document.getElementById("partnerDataInput");

        groupId = document.getElementById("groupId");
        permissions = document.getElementById("permissions");
        screenName = document.getElementById("screenName");
        siteUrl = document.getElementById("siteUrl");
        mediaTypeInput = document.getElementById("mediaTypeInput");
}
&lt;/script&gt;
</pre>
  </div>
  
  <div>
    To allow maximum workflow flexibility, each method implements a specific functionality. These functionalities may be used/combined/altered according to workflow requirements. The list below describes the method's signature and whether the method is JS enabled.
  </div>
</div>

<table>
  <thead>
    <tr>
      <th>
        Method Signature
      </th>
      
      <th>
        Description
      </th>
      
      <th>
        JS enabled
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        upload():void
      </td>
      
      <td style="text-align: left;">
        The upload method activates Kaltura upload services for uploading all media files selected at the desktop browser within the current session. If the upload process was previously stopped, it will start from the file whose upload was cancelled.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setTags(tags:Array, startIndex:int, endIndex:int):void
      </td>
      
      <td style="text-align: left;">
        The setTags method overrides existing tags for the selected media file/s. The startIndex and endIndex parameters indicate the specific media files that this tag applies to. Set StartIndex to 0 for the first selected file.<br />For example: A user selects 5 media files: f1,f2,f3,f4,f5. Then tag1 is  set at startIndex=2 and endIndex=4. tag1 will override all existing tags for f3,f4,f5.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        addTags(tags:Array, startIndex:int, endIndex:int):void
      </td>
      
      <td style="text-align: left;">
        The addTags method adds tags for the selected media file/s. The startIndex and endIndex parameters indicate the specific media files that this tag should be added for. Set StartIndex to 0 for the first selected file.<br />For example: A user selects 5 media files: f1,f2,f3,f4,f5. Then tag1 is  set at startIndex=2 and endIndex=4. tag1 will be added to the existing tags of f3,f4,f5.
      </td>
      
      <td>
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setTitle(title:String, startIndex:int, endIndex:int):void
      </td>
      
      <td style="text-align: left;">
        The SetTitle method sets titles for the selected media file/s. The startIndex and endIndex parameters indicate the specific media files that this title should be set for. Set StartIndex to 0 for the first selected file.<br />For example: A user selects 5 media files: f1,f2,f3,f4,f5. Then title1 is  set at startIndex=2 and endIndex=4. title1 will be set to f3,f4,f5.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        getFiles():Array 
      </td>
      
      <td style="text-align: left;">
        <span>The getFiles method retrieves an array of Kaltura entry objects for the selected media files. Each entry object contains metadata and other information including entryId, if already available.</span>
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        addEntries():void
      </td>
      
      <td style="text-align: left;">
        The addEntries method activates Kaltura entry creation services. This is the final step in uploading media files. An entry is created for each uploaded file and an entryId is generated as a unique identifier for the uploaded media within the Kaltura system.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        stopUploads():void
      </td>
      
      <td style="text-align: left;">
        The stopUploads method activates Kaltura services to abort the current upload process.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setMaxUploads(value:uint):void
      </td>
      
      <td style="text-align: left;">
        The setMaxUploads method overrides the current limit of maximum number of files to be selected by end-users at the desktop browser in one session. This value can also be pre-populated within the flashVars array.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setPartnerData(value:String):void
      </td>
      
      <td style="text-align: left;">
        The setPartnerData method sets an additional site-specific metadata field to the uploaded media. This value can also be pre-populated within the flashVars array.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setMediaType(mediaType:String):void
      </td>
      
      <td style="text-align: left;">
        The setMediaType sets the media type to show in the file dialogue. The media types are defined in the uiConf file. The common types to be set as arguments for this method are: “video”, “audio”, “image”
      </td>
      
      <td>
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setGroupId(value:String):void
      </td>
      
      <td style="text-align: left;">
        The setGroupId method sets the group ID. This value can also be pre-populated within the flashVars array.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setPermissions(value:String):void
      </td>
      
      <td style="text-align: left;">
        The setPermissions method sets the permission level. This value can also be pre-populated within the flashVars array.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setSiteUrl(value:String):void
      </td>
      
      <td style="text-align: left;">
        The setSiteUrl method sets the site URL as a metadata parameter.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        setScreenName(value:String):void
      </td>
      
      <td style="text-align: left;">
        The setScreenName method sets the screen name of the uploading user, when applicable.
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        getError():String
      </td>
      
      <td style="text-align: left;">
        The getError method returns the current error if any exists. Otherwise it returns null. Possible values: “fileSizeExceeds”, ”totalSizeExceeds”, ”numFilesExceeds”, ”uploadError”
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
  </tbody>
</table>

## <a name="ConstructKalturaObjects"></a>Construct Kaltura Objects for Session Initiation and Populate Variables to be Passed to the Embedded Flash Object

In the example above, two constants and one variable are defined that are used later within the implementation. The PHP code constructs the relevant Kaltura objects used for session initiation. The objects are constructed as defined and implemented in the relevant Kaltura API Client Library.

<div>
  <div>
    <pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;body onload=onLoadHandler()&gt;
&lt;?php
//define constants
define("KALTURA_PARTNER_ID", Your Partner ID);
define("KALTURA_PARTNER_WEB_SERVICE_SECRET", "Your Partner Web Service Secret");
 

//define session variables
$partnerUserID          = 'myUploaderUser@domain.com'; //Make sure to replace "myUploaderUser@domain.com" with your system user id.
//When allowing anonymous uploads, make sure to create a new user in the Kaltura system that has only upload permissions, then set partnerUserID to the that user.
//Construction of Kaltura objects for session initiation

$config           = new KalturaConfiguration(KALTURA_PARTNER_ID);
$client           = new KalturaClient($config);
$ks               = $client-&gt;session-&gt;start(KALTURA_PARTNER_WEB_SERVICE_SECRET, $partnerUserID,KalturaSessionType::USER);

$flashVars = array();

$flashVars["uid"]   = $partnerUserID; 
$flashVars["partnerId"]                         = KALTURA_PARTNER_ID;
$flashVars["subPId"]                    = KALTURA_PARTNER_ID*100;
$flashVars["ks"]   = $ks; 
$flashVars["conversionProfile"]   = 5; 
$flashVars["maxFileSize"]   = 10; 
$flashVars["maxTotalSize"]   = 50; 
$flashVars["uiConfId"]   = 7578522; 
$flashVars["jsDelegate"]   = "delegate";
$flashVars["entryId"] = -1; 
?&gt;</pre>
  </div>
  
  <div>
    The following lists the parameters and their descriptions.
  </div>
</div>

<table>
  <thead>
    <tr>
      <th>
        Parameter
      </th>
      
      <th>
        Type
      </th>
      
      <th>
        Default
      </th>
      
      <th>
        Description
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        KALTURA_PARTNER_ID
      </td>
      
      <td style="text-align: left;">
        Numeric
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
      
      <td style="text-align: left;">
        Enter your partner ID. <span>Please refer to </span><a href="http://knowledge.kaltura.com/kaltura-api-usage-guidelines">Kaltura API usage guidelines</a>.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        KALTURA_PARTNER_WEB_SERVICE_SECRET
      </td>
      
      <td style="text-align: left;">
        String
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
      
      <td style="text-align: left;">
        Enter your Web Service Secret. <span>Please refer to </span><a href="http://knowledge.kaltura.com/kaltura-api-usage-guidelines">Kaltura API usage guidelines</a>. This Secret string is used in Kaltura objects to create a secure session ID, preventing hacking and abuse attempts that intend  to damage a partner/end-user’s content.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        partnerUserID
      </td>
      
      <td style="text-align: left;">
        String
      </td>
      
      <td style="text-align: left;">
        “myUploaderUser@ domain.com”
      </td>
      
      <td style="text-align: left;">
        <p>
          Enter your internal system end-user identifier. This variable is used to relate the uploaded content to its uploading user. It may be used by Kaltura partners for user management and statistics tracking.
        </p>
        
        <p>
          When enabling anonymous uploads, create a new user in the Kaltura system (through the KMC Administration panel) and set this user's permissions to only allow upload of content.
        </p>
        
        <p>
          Note - This user should be unique and correlate with your system user ids. Assigning all upload sessions with the same user id will associate all the videos with the same user id, and allow anyone who captures that user session to delete or modify all videos uploaded using that user session. In cases where the uploading user is anonymous on your site, make sure to use a session that is limitted to the upload permission only. For more details about API Authentication and Security, refer to <a href="{{site.url}}/documentation/Knowledge/kalturas-api-authentication-and-security.html">Kaltura's API Authentication and Security</a>.
        </p>
      </td>
    </tr>
  </tbody>
</table>

 

In the example above, the PHP/JavaScript code prepares the flashVars array, which is passed later to the embedded object.

Below is a description of some applicative parameters that are transferred to the KSU flash object via the flashVars array.   
Some of these variables are set by an internal configuration xml as well. Passing these parameters at the flashVars array overrides this configuration:

<table>
  <thead>
    <tr>
      <th>
        Parameter
      </th>
      
      <th>
        Description
      </th>
      
      <th>
        Data Type/Required
      </th>
      
      <th>
        Defined in Widget ConfUI xml
      </th>
      
      <th>
        Default
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        $flashVars["uid "]
      </td>
      
      <td style="text-align: left;">
        The end-user internal identifier
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["partnerId"]
      </td>
      
      <td style="text-align: left;">
        The Partner ID
      </td>
      
      <td style="text-align: left;">
        Int/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["subPId"]
      </td>
      
      <td style="text-align: left;">
        The Sub Partner ID. The value should equal Partner_ID*100
      </td>
      
      <td style="text-align: left;">
        Int/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["entryId"]
      </td>
      
      <td style="text-align: left;">
        Internal Parameter - Mandatory
      </td>
      
      <td style="text-align: left;">
        Int/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["ks"]
      </td>
      
      <td style="text-align: left;">
        The unique Kaltura session ID generated by Kaltura API Client objects
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["conversionProfile"]
      </td>
      
      <td style="text-align: left;">
        Sets the media conversion method to be applied on the uploaded media file
      </td>
      
      <td style="text-align: left;">
        Int/Optional
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
      
      <td style="text-align: left;">
        5
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["maxFileSize"]
      </td>
      
      <td style="text-align: left;">
        Sets a restriction on the maximum file size to be applied to the uploaded media file
      </td>
      
      <td style="text-align: left;">
        Int/Optional
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["maxTotalSize"]
      </td>
      
      <td style="text-align: left;">
        Sets a restriction on the total maximum file sizes to be applied within one upload session
      </td>
      
      <td style="text-align: left;">
        Int/Optional
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
      
      <td style="text-align: left;">
         
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["uiConfId"]
      </td>
      
      <td style="text-align: left;">
        The configuration xml IDof the KSU widget
      </td>
      
      <td style="text-align: left;">
        Int/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        7578522
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["jsDelegate"]
      </td>
      
      <td style="text-align: left;">
        The exact name of the array of JS handler methods
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        No
      </td>
      
      <td style="text-align: left;">
        “delegate” 
      </td>
    </tr>
  </tbody>
</table>

## <a name="SettheLocation"></a>Set the Location of the Transparent KSU Widget and Embed Flash Object 

The following example shows a flashContainer div that is set to contain the transparent flash object of the KSU widget.

<pre class="brush: jscript;fontsize: 100; first-line: 1; ">&lt;div id="flashContainer"&gt;
        &lt;form&gt;
                &lt;input type="button" value="Step 1 - Browse & Select"&gt;
        &lt;/form&gt;
        &lt;div id="uploader"&gt; 
        &lt;/div&gt;
        &lt;script language="JavaScript" type="text/javascript"&gt;
                var params = {
                        allowScriptAccess: "always",
                        allowNetworking: "all",
                        wmode: "transparent"
 

                };
                var attributes  = {
                        id: "uploader",
                        name: "KUpload"
                };
                // set flashVar object
                var flashVars = &lt;?php echo json_encode($flashVars); ?&gt;;
                 &lt;!--embed flash object--&gt;
                swfobject.embedSWF("http://www.kaltura.com/kupload/ui_conf_id/7578522", "uploader", "200","30", "9.0.0", "expressInstall.swf", flashVars, params,attributes);
        &lt;/script&gt;
&lt;/div&gt;
</pre>

 

The KSU widget must be located on top of the actual GUI element that your end-users interact with when they want to open a desktop browser. This is needed to overcome a flash security restriction, and allows browse operations to be triggered as a result of user-interaction.

The following image shows the transparent KSU widget (marked with the dotted line) located on top of a functionless “Select & Browse” button (set within an html span tag in the example). This way the desktop browser is triggered from the KSU widget itself when clicking the button.

<img src="{{site.url}}/assets/419">

The uploader div is set as a SWFObject’s alternative content container. Refer to <a href="http://code.google.com/p/swfobject/wiki/documentation" target="_blank">Google hosted SWFObject documentation</a> for more information on why this configuraiton is necessary. Make sure that the ID of this div element is the same as the ID of the embedded flash object.

The params and attributes variables are set. Make sure their elements are set as in the above example to allow object transparency and proper communication with the KSU widget.

Finally, a JavaScript call to swfobject.embedSWF function is made. This actually embeds the KSU widget. The applicative parameters that are passed as arguments in this example are:

<table>
  <thead>
    <tr>
      <th>
        Parameter
      </th>
      
      <th>
        Type/Required
      </th>
      
      <th>
        Default/Suggested
      </th>
      
      <th>
        Description
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        Flash File URL
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        http://www.kaltura.com/kupload/ui_conf_id/7578522
      </td>
      
      <td style="text-align: left;">
        The file path and name of the KSU flash file
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        ID
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        “uploader”
      </td>
      
      <td style="text-align: left;">
        The ID of embedded object. Make sure this string is the same as the name of the alternative content div for the SWFObject to operate properly.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        width
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
         
      </td>
      
      <td style="text-align: left;">
        The width of the transparent KSU Flash Object
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        height
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        “30”
      </td>
      
      <td style="text-align: left;">
        The height of the transparent KSU Flash Object
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        Version
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        "9.0.0"
      </td>
      
      <td style="text-align: left;">
        Specifies the Flash player version that the KSU flash object is published for
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        ExpressInstallSwfurl
      </td>
      
      <td style="text-align: left;">
        String/Optional
      </td>
      
      <td style="text-align: left;">
        “false”
      </td>
      
      <td style="text-align: left;">
        Specifies the URL of your express install SWF and activates Adobe express install when needed. When set to “false”, the express install is not activated.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        FlashVars
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
      
      <td style="text-align: left;">
        Applicative information in flashvars array of name:value pairs
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        Params
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
         var params = {<p>
                  allowScriptAccess:"always",
        </p>
        
        <p>
                  allowNetworking: "all",
        </p>
        
        <p>
                  wmode: "transparant"
        </p>
        
        <p>
          };
        </p>
      </td>
      
      <td style="text-align: left;">
        Flash object generic parameters in an array of  name:value pairs. Make sure vmode is set to transparent.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        Attributes
      </td>
      
      <td style="text-align: left;">
        String/Required
      </td>
      
      <td style="text-align: left;">
         var attributes = {<p>
                   name: "KUpload",
        </p>
        
        <p>
                  id: "uploader"
        </p>
        
        <p>
          };
        </p>
      </td>
      
      <td style="text-align: left;">
        Object attributes in an array of name:value pairs. The name attribute must be “KUpload”. The id attribute can be set to the ID you assign to your object and to your SWFObject alternative content div.
      </td>
    </tr>
  </tbody>
</table>

For more information on the swfobject.embedSWF method, see the <a href="http://code.google.com/p/swfobject/wiki/documentation" target="_blank">Google hosted SWFObject documentation page</a>. 

## <a name="OptionalImplementInputFields"></a>(Optional) Implement Input Fields for Dynamic User Input 

The following example displays a few interactive form fields that are set to enable Kaltura partner’s integrators to test and activate Kaltura services using the KSU Widget. These forms were set for example purposes only. Please use the relevant methods according to your web application workflow.

<div>
  <pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;div id="userInput"&gt;
        &lt;input type="button" value="Step 2 - Upload" onclick="upload()"&gt;
        &lt;input type="button" value="Step 3 - Add entries" onclick="addEntries()"&gt;
        &lt;input type="button" value="Cancel" onclick="stopUploads()"&gt;
 
        &lt;input type="text" id="mediaTypeInput" /&gt;
        &lt;input type="button" value="Set media type" onclick="setMediaType()"&gt;

        &lt;input type="button" value="Get Files Objects " onclick="getFiles()"&gt;

        &lt;input type="text" value="enter tags here" id="tagsInput" /&gt;
        &lt;input type="text" value="0" id="tagsStartIndex" /&gt;
        &lt;input type="text" value="0" id="tagsEndIndex" /&gt;
        &lt;input type="button" value="Add tags" onclick="addTagsFromForm()"&gt;
        &lt;input type="button" value="Set tags" onclick="setTagsFromForm()"&gt;

        &lt;input type="text" value="enter title here" id="titleInput" /&gt;
        &lt;input type="text" value="0" id="titleStartIndex" /&gt;
        &lt;input type="text" value="0" id="titleEndIndex" /&gt;
        &lt;input type="button" value="Set title" onclick="setTitleFromForm()"&gt;

        &lt;input type="text" value="0" id="removeStartIndex" /&gt;
        &lt;input type="text" value="0" id="removeEndIndex" /&gt;
        &lt;input type="button" value="Remove Files" onclick="removeFilesFromForm()"&gt;

        &lt;input type="text" value="0" id="maxUploadsInput" /&gt;
        &lt;input type="button" value="Set max uploads"onclick="setMaxUploads(parseInt(maxUploadsInput.value))"&gt;

        &lt;input type="text" value="partner data goes here" id="partnerDataInput" /&gt;
        &lt;input type="button" value="Set partner data" onclick="setPartnerData(partnerDataInput.value)"&gt;
        &lt;input id="groupId" /&gt;
        &lt;input type="button" value="set group id " onClick="setGroupId(groupId.value)"&gt;
        &lt;input id="permissions" /&gt;
        &lt;input type="button" value="set permissions" onClick="setPermissions(permissions.value)"&gt;
        &lt;input id="screenName" /&gt;
        &lt;input type="button" value="Set screen name" onClick="setScreenName(screenName.value)"&gt;
        &lt;input id="siteUrl" /&gt;
        &lt;input type="button" value="set site url" onClick="setSiteUrl(siteUrl.value)"&gt;
&lt;/div&gt;</pre>
</div>

## Errors – Flash Player Exceptions

The following errors may occur:

*   Limitations error – "Cannot upload, limitations exceeded. Please check for errors"  
    Thrown if the upload() function is invoked while an error exists.
*   Upload error - "Cannot add entries, some uploads failed. Either re-upload or remove the files"  
    Thrown if the addEntries() function is invoked while an error exists.

Errors may be polled by calling getError();