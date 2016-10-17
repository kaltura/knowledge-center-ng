---
layout: page
title: "Kaltura Contributor Wizard (KCW) - Website Integration "
date: 2012-03-27 01:26:48
---

<h2 class="admin-note">
  Prerequisites
</h2>

<ul class="bb-list">
  <li>
    Kaltura KCW widget: 2.1.6
  </li>
  <li>
    Kaltura Partner Service: 3.0 (api_v3)
  </li>
</ul>

## Usage

The Kaltura Contributor Wizard (KCW) is a standalone GUI widget enabling content administrators and/or web sites’ end-users to conveniently upload and use video, image and audio media files.  See <a href="http://knowledge.kaltura.com/kaltura-contribution-wizard-kcw" class="bb-url">Overview of the KCW widget</a>.

## Integration Steps

<span>To get started please read </span>[Kaltura API usage guidelines][1].

 [1]: http://knowledge.kaltura.com/kaltura-api-usage-guidelines

<a name="edit-web-page"></a>

## Edit your Web Page to Integrate with the Kaltura Contributor Wizard widget

Integrating the KCW Widget into your website requires that you add the following into your web page:

<ul class="bb-list">
  <li>
    <a href="#ext">Inclusion of External Scripts</a>
  </li>
  <li>
    <a href="#constants">Definition of Constants and Variables</a>
  </li>
  <li>
    <a href="#construct">Construction of Kaltura Objects for Session Initiation</a>
  </li>
  <li>
    <a href="#passing">Population of Variables to be Passed to Embedded Flash Object</a>
  </li>
  <li>
    <a href="#embed">Embedding of Flash Objects</a>
  </li>
  <li>
    <a href="#callback">Callback methods communicating with widget events</a>
  </li>
  <li>
    <a href="#passing">Dynamic partner’s data and external control on widget steps (advanced and optional)</a>
  </li>
</ul>

## Full Example Script

The following example of PHP/JavaScript script demonstrates the integration of the KCW Widget into a PHP based web application.   
To run this script,be certain that you set your partner identifiers for the <span class="geshifilter"><code class="geshifilter-php">KALTURA_PARTNER_ID</code></span> and <span class="geshifilter"><code class="geshifilter-php">KALTURA_PARTNER_SERVICE_SECRET&nbsp;</code></span>constants.   
Look for detailed information on this example in the following sections:

<div class="geshifilter">
  <div class="html4strict geshifilter-html4strict">
    {% highlight javascript %}
<html> <head> <!--include external scripts--> 
<?php require_once("KalturaClient.php"); ?> 
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/swfobject/2.2/swfobject.js"></script>
</head>
<body>
<?php //define constants define("KALTURA_PARTNER_ID", Your Kaltura Partner ID); 
define("KALTURA_PARTNER_SERVICE_SECRET", "Your Kaltura Service Secret"); 
//define session variables $partnerUserID = 'ANONYMOUS'; //construct Kaltura objects for session initiation 
$config = new KalturaConfiguration(KALTURA_PARTNER_ID); 
$client = new KalturaClient($config); 
$ks = $client->session->start(KALTURA_PARTNER_SERVICE_SECRET, $partnerUserID, KalturaSessionType::USER); //Prepare variables to be passed to embedded flash object. 
$flashVars = array(); 
$flashVars["uid"] = $partnerUserID; 
$flashVars["partnerId"] = KALTURA_PARTNER_ID; 
$flashVars["ks"] = $ks; 
$flashVars["afterAddEntry"] = "onContributionWizardAfterAddEntry"; 
$flashVars["close"] = "onContributionWizardClose"; 
$flashVars["showCloseButton"] = false; 
$flashVars["Permissions"] = 1; 
?> 
<div id="kcw"></div> <script type="text/javascript"> 
var params = { allowScriptAccess: "always", allowNetworking: "all", wmode: "opaque" }; // php to js 
var flashVars = <?php echo json_encode($flashVars); ?>; 
<!--embed flash object--> 
swfobject.embedSWF("http://www.kaltura.com/kcw/ui_conf_id/1000741 ", "kcw", "680", "360", "9.0.0", "expressInstall.swf", flashVars, params); 
</script>
<!--implement callback scripts--> 
<script type="text/javascript"> 
function onContributionWizardAfterAddEntry(entries) 
{ 
	alert(entries.length + " media file/s was/were succsesfully uploaded"); 
	for(var i = 0; i < entries.length; i++) { 
		alert("entries["+i+"]:EntryID = " + entries[i].entryId); 
	} 
} 
</script> 
<script type="text/javascript"> 
function onContributionWizardClose() 
{ 
	alert("Thank you for using Kaltura ontribution Wizard"); 
} 
</script>
</body>
</html>
{% endhighlight %}
  </div>
</div>

## <a name="ext"></a>Inclusion of External Scripts

The KalturaClient.php script is part of the PHP Kaltura API Client Library being included to enable the use of Kaltura objects. The swfobject.js script is the <a href="http://code.google.com/p/swfobject/" class="bb-url">Google hosted SWFObject</a>, being used for embedding the KCW widget as a flash object.

<div class="geshifilter">
  <div class="html4strict geshifilter-html4strict">
    {% highlight javascript %}
<head> <!--include external scripts--> 
<?php require_once("KalturaClient.php"); ?> 
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/swfobject/2.2/swfobject.js"></script> 
</head>
{% endhighlight %}
  </div>
</div>

## <a name="constants"></a>Define Constants and Variables

In the following example, the PHP code defines 2 constants and one variable, later to be used within implementation.

<div class="geshifilter">
  <div class="php geshifilter-php">
    {% highlight php %}
//define constants define("KALTURA_PARTNER_ID", Your Kaltura Partner ID); 
define("KALTURA_PARTNER_SERVICE_SECRET", "Your Kaltura Service Secret"); //define session variables 
$partnerUserID = 'ANONYMOUS';
{% endhighlight %}
  </div>
</div>

The following lists the constants and variable parameters and their descriptions.

<table>
  <thead>
    <tr>
      <th>
        Parameter
      </th>
      
      <th>
        Data Type
      </th>
      
      <th>
        Default Value
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
      
      <td>
        Numeric
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
      
      <td style="text-align: left;">
        Enter your Partner ID. <span>Please refer to </span><a href="http://knowledge.kaltura.com/kaltura-api-usage-guidelines">Kaltura API usage guidelines</a>.
      </td>
    </tr>
    
    <tr>
      <td>
        KALTURA_PARTNER_SERVICE_SECRET
      </td>
      
      <td style="text-align: left;">
        String
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
      
      <td style="text-align: left;">
        Enter your Web Service Secret. R<span>efer to </span><a href="http://knowledge.kaltura.com/kaltura-api-usage-guidelines">Kaltura API usage guidelines</a> for more information. The Secret string is used within Kaltura objects to create a secured session ID, preventing hacking and abuse attempts aiming to damage Partner/end-user’s content.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        partnerUserID
      </td>
      
      <td style="text-align: left;">
        String
      </td>
      
      <td>
        "ANONYMOUS"
      </td>
      
      <td style="text-align: left;">
        Use to populate your internal system end-user identifier. This variableis  used to relate the uploaded content to its uploading user, and be used by Kaltura partners for user management and statistics tracking.
      </td>
    </tr>
  </tbody>
</table>

## <a name="construct"></a>Construct Kaltura Objects for Session Initiation

In the following example, the PHP code constructs the relevant Kaltura objects that are used for session initiation. The objects are constructed as defined and implemented in the relevant Kaltura API Client Library.

<div class="geshifilter">
  <div class="php geshifilter-php">
    {% highlight php %}
//construct Kaltura objects for session initiation 
$config = new KalturaConfiguration(KALTURA_PARTNER_ID); 
$client = new KalturaClient($config); 
$ks = $client->session->start(KALTURA_PARTNER_SERVICE_SECRET, $partnerUserID,KalturaSessionType::USER);
{% endhighlight %}
  </div>
</div>

 

## <a name="prepare"></a>Prepare Variables to be Passed to Embedded Flash Object

In the following example, the PHP/JavaScript code is preparing the flashVars and params variables to be passed to the embedded object.

<div class="geshifilter">
  <div class="php geshifilter-php">
    {% highlight javascript %}
<?php
//Prepare variables to be passed to embedded flash object. 
$flashVars = array(); 
$flashVars["uid"] = $partnerUserID; 
$flashVars["partnerId"] = KALTURA_PARTNER_ID; 
$flashVars["ks"] = $ks; 
$flashVars["afterAddEntry"] = "onContributionWizardAfterAddEntry"; 
$flashVars["close"] = "onContributionWizardClose"; 
$flashVars["showCloseButton"] = false; 
$flashVars["Permissions"] = 1; 
?> 
<div id="kcw"></div> 
<script type="text/javascript"> 
var params = { allowScriptAccess: "always", allowNetworking: "all", wmode: "opaque" }; // php to js 
var flashVars = <?php echo json_encode($flashVars); ?>; 
{% endhighlight %}
  </div>
</div>

Below is a description of some applicative parameters that are transferred to the KCW flash object via the flashVars array. Some of these variables are also set in an internal configuration xml. Passing these parameters at the flashVars array will override this configuration:

<table align="left">
  <thead>
    <tr>
      <th>
        Parameter
      </th>
      
      <th>
        Description
      </th>
      
      <th>
        Data Type
      </th>
      
      <th>
        Required / Optional
      </th>
      
      <th>
        Defined in Widget Config xml
      </th>
      
      <th>
        Default Value
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;">
        $flashVars["uid"]
      </td>
      
      <td style="text-align: left;">
        This is the end-user internal identifier
      </td>
      
      <td>
        String
      </td>
      
      <td>
        Required
      </td>
      
      <td>
        No
      </td>
      
      <td>
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["partnerId"]
      </td>
      
      <td style="text-align: left;">
        This is the Partner ID
      </td>
      
      <td>
        String
      </td>
      
      <td>
        Required
      </td>
      
      <td>
        No
      </td>
      
      <td>
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["ks"]
      </td>
      
      <td style="text-align: left;">
        This is the unique Kaltura session ID as was generated by Kaltura API Client objects
      </td>
      
      <td>
        String
      </td>
      
      <td>
        Required
      </td>
      
      <td>
        No
      </td>
      
      <td>
        N/A
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["afterAddEntry"]
      </td>
      
      <td style="text-align: left;">
        This is the name of the JavaScript function to be implemented as a callback for the afterAddEntry event of the KCW widget. The callback mechanism is described at the<a href="#define-and-implement" class="bb-url">“Define and implement callback methods to be activated upon widget events” section</a>
      </td>
      
      <td>
        String
      </td>
      
      <td>
        Required
      </td>
      
      <td>
        No
      </td>
      
      <td>
        "afterAddEntry"
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["close"]
      </td>
      
      <td style="text-align: left;">
        This is the name of the JavaScript function to be implemented as a callback for the close event of the KCW widget; it is being triggered upon pressing the close button of the widget (when enabled), or upon pressing the ‘finish’ button after a successful uploading. The callback mechanism is described at the<a href="#define-and-implement" class="bb-url">“Define and implement callback methods to be activated upon widget events” section</a>
      </td>
      
      <td>
        String
      </td>
      
      <td>
        Required
      </td>
      
      <td>
        No
      </td>
      
      <td>
        "close"
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["showCloseButton"]
      </td>
      
      <td style="text-align: left;">
        This variable controls the use of the KCW close button. When this variable is set to false, no close button will appear within the KCW widget. It makes sense to hide this button when the KCW widget is an integral part of your web page. When you embed the KCW widget within a lightbox layer, you may choose to show the close button, by setting this variable to true.
      </td>
      
      <td>
        Boolean
      </td>
      
      <td>
        Optional
      </td>
      
      <td>
        Yes
      </td>
      
      <td>
        True
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        $flashVars["Permissions"]
      </td>
      
      <td style="text-align: left;">
        This variable defines who will be able to see the uploaded media file.<ol class="bb-list">
          <li>
            public
          </li>
          <li>
            private
          </li>
          <li>
            group
          </li>
          <li>
            friends
          </li>
        </ol>
      </td>
      
      <td>
        int
      </td>
      
      <td>
        Optional
      </td>
      
      <td>
        No
      </td>
      
      <td>
        1
      </td>
    </tr>
  </tbody>
</table>

The flashVars array being populated at the above example should be transferred into an appropriate format, using php json_encode method, just before being transferred into the embedded object.

## <a name="embed"></a>Embed Flash Objects

The following example shows how a JavaScript call to <span class="geshifilter"><code class="geshifilter-javascript">swfobject.embedSWF</code></span> function is being made; this is the actual embedding of the KCW Widget. {% highlight javascript %}
<!--embed flash object--> 
swfobject.embedSWF("http://www.kaltura.com/kcw/ui\_conf\_id/1000199", "kcw", "680", "360", "9.0.0","expressInstall.swf", flashVars, params); </script> 
{% endhighlight %}

The applicative parameters being passed as arguments at this example are:

<div class="geshifilter">
  <div class="javascript geshifilter-javascript">
     
  </div>
</div>

<table>
  <thead>
    <tr>
      <th>
        Parameter
      </th>
      
      <th>
        Data Type
      </th>
      
      <th>
        Required/Optional
      </th>
      
      <th>
        Default Value
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
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        The url should be constructed in the following template:<br />http://{kaltura_server_domain}/kcw/ui_conf_id/{id_of_uiconf}<br />If you are using the hosted edition on Kaltura.com, the following two are available as a start:<ul class="bb-list">
          <li>
            Dark colors widget: http://www.kaltura.com/kcw/ui_conf_id/1000740
          </li>
          <li>
            Light color widget: http://www.kaltura.com/kcw/ui_conf_id/1000741
          </li>
        </ul>
      </td>
      
      <td style="text-align: left;">
        The file path and name of the KCW flash file at a specific Look & Feel.
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        ID
      </td>
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        "kcw"
      </td>
      
      <td style="text-align: left;">
        Id of embedded object
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        width
      </td>
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        You should use "680"
      </td>
      
      <td style="text-align: left;">
        The width of the KCW Flash Object
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        height
      </td>
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        You should use "360"
      </td>
      
      <td style="text-align: left;">
        The height of the KCW Flash Object
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        Version
      </td>
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        KCW require Flash Player 9 and above, so use: "9.0.0"
      </td>
      
      <td style="text-align: left;">
        Specifies the Flash player version the KCW flash object is published for
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        ExpressInstallSwfurl
      </td>
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Optional
      </td>
      
      <td style="text-align: left;">
        “false”
      </td>
      
      <td style="text-align: left;">
        Specifies the URL of your express install SWF and activates Adobe express install when needed. When set to “false” the express install will not be activated
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        FlashVars
      </td>
      
      <td style="text-align: left;">
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
      
      <td style="text-align: left;">
        Applicative information for flashvars object constructed as such {parameter1_name:parameter1_value,parameter2_name:parameter2_value} pairs
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        Params
      </td>
      
      <td>
        String
      </td>
      
      <td style="text-align: left;">
        Required
      </td>
      
      <td style="text-align: left;">
        We recommand using the following: [javascipt]var params = {<br />allowScriptAccess: "always",<br />allowNetworking: "all",<br />wmode: "opaque"<br />};[/javascipt]
      </td>
      
      <td style="text-align: left;">
        flash object generic parameters constructed as such {parameter1_name:parameter1_value,parameter2_name:parameter2_value} pairs
      </td>
    </tr>
  </tbody>
</table>

Please look for more information on the [javascipt]swfobject.embedSWF[/javascipt] method at <a href="http://code.google.com/p/swfobject/wiki/documentation" class="bb-url">Google SWFObject documentation page</a>.

<a name="define-and-implement"></a>

## <a name="callback"></a>Define and Implement Callback Methods to be Activated upon Widget Events

<div class="geshifilter">
  <div class="javascript geshifilter-javascript">
    {% highlight javascript %}
<!--implement callback scripts--> 
<script type="text/javascript"> 
function onContributionWizardAfterAddEntry(entries) 
{ 
	alert(entries.length + " media file/s was/were succsesfully uploaded"); 
	for(var i = 0; i < entries.length; i++) { 
		alert("entries["+i+"]:EntryID = " + entries[i].entryId); 
	} 
} 
</script>
{% endhighlight %}
{% highlight javascript %}
<script type="text/javascript"> 
function onContributionWizardClose() 
{ 
	alert("Thank you for using Kaltura Contribution Wizard"); 
} 
</script> 
{% endhighlight %}
  </div>
</div>

Kaltura enables developers to implement event based communication between the KCW Widget and their web applications. This is achieved by using the JavaScript callback functions, implemented by developers, according to the applicative needs of their web sites. The KCW communicates with web application upon 2 events:

<table>
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
    <tr>
      <td style="text-align: left;">
        <span>Configurable and determined by flashVars</span><br /><span class="geshifilter"><code class="geshifilter-javascript">afterAddEntry&nbsp;&lt;span>=&lt;/span>&nbsp;callback ID</code></span><br /><span>at the example:</span><br /><span class="geshifilter"><code class="geshifilter-javascript">afterAddEntry&nbsp;&lt;span>=&lt;/span>onContributionWizardAfterAddEntry</code></span>
      </td>
      
      <td style="text-align: left;">
        This event is being triggered upon a completion of content (Entry) uploading.
      </td>
      
      <td style="text-align: left;">
        Entries = array of FileVO objects. <br />Each FileVO object contains information for the uploaded media file.<br /><br />at the example:<br />Entries[i].entryId represents the unique identifier of the uploaded media within the Kaltura system. <br />It may be used to integrate the KCW widget with other widgets/applications<br />Entries[i].MediaType represents the media type of the uploaded media<br />Video=1/image=2/Audio= 5
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;">
        <span>Configurable and determined by flashVars</span><br /><span class="geshifilter"><code class="geshifilter-javascript">&lt;span>close&lt;/span>&nbsp;&lt;span>=&lt;/span>&nbsp;callback ID</code></span><br /><span>at the example:</span><br /><span class="geshifilter"><code class="geshifilter-javascript">&lt;span>close&lt;/span>&nbsp;&lt;span>=&lt;/span>&nbsp;onContributionWizardClose</code></span>
      </td>
      
      <td style="text-align: left;">
        This event is being triggered upon a completion of content (Entry) uploading.
      </td>
      
      <td style="text-align: left;">
        N/A
      </td>
    </tr>
  </tbody>
</table>

## <a name="passing"></a>Passing Partner Data to the KCW Widget

Kaltura partner’s site-specific workflow may require the KCW Widget to receive and store additional data per uploaded content. While Kaltura provides several generic metadata fields attached to each entry, such as title and tags, it is sometimes necessary to relate additional site-specific data to the uploaded content. Kaltura enables this metadata flexibility by supporting a dedicated partner data field. This field may contain up to 1K characters and can include an XML structure if multiple parameters are needed.

Partner’s data is being handled differently in the 2 following cases:

<ul class="bb-list">
  <li>
    <span>Static Partner data</span><br />Partner data is available before the KCW Widget is embedded. This is mainly the case when partner data is constant within the same web page. For example, you allow content uploading from several locations on your website and you want to relate the uploaded content to the exact URL it was uploaded from.<br />In this case an additional flashVar pair should be added when preparing the flashVar array before embedding the KCW Widget.<table>
      <thead>
        <tr>
          <th>
            Parameter
          </th>
          
          <th>
            Description
          </th>
          
          <th>
            Data Type
          </th>
          
          <th>
            Required
          </th>
          
          <th>
            Defined in Widget Config xml
          </th>
          
          <th>
            Default Value
          </th>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td>
            $flashVars["partnerData"]
          </td>
          
          <td style="text-align: left;">
            This parameter will hold any partner specific data and will store it with every uploaded content entry. It is possible to use this parameter to pass more than one data item within an XML structure. This field may contain up to 1K characters
          </td>
          
          <td>
            String
          </td>
          
          <td>
            Optional
          </td>
          
          <td>
            No
          </td>
          
          <td>
            N/A
          </td>
        </tr>
      </tbody>
    </table>
  </li>
  
  <li>
    <span>Dynamic Partner data</span><br />Partner data is not available before the KCW Widget is embedded. This is mainly the case when partner data relies on end-user interaction. For example, you want your end-users to be able to relate their uploaded content with a specific filter which you want to use for specific purpose within your website.<p>
      In this case the KCW flash object should be updated with the additional data when it’s available using KCW’s public method<span class="geshifilter"><code class="geshifilter-javascript">setPartnerData</code></span>. 
    </p>
    
    <table>
      <thead>
        <tr>
          <th>
            Method signature
          </th>
          
          <th>
            Description
          </th>
          
          <th>
            JS Enabled
          </th>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td>
            <span class="geshifilter"><code class="geshifilter-javascript">setPartnerData&lt;span>(&lt;/span>value&lt;span>:*&lt;/span>&lt;span>)&lt;/span>&lt;span>:&lt;/span>&lt;span>void&lt;/span></code></span>
          </td>
          
          <td>
            Sets the partner data
          </td>
          
          <td>
            Yes
          </td>
        </tr>
      </tbody>
    </table>
    
    <p>
      In the example below, partner data could be set by end-users at the partnerData text field. Clicking the ‘set partner data’ button activates a java script function that passes this data to the KCW flash object (identified by its “kcw”id).
    </p>
    
    <div class="geshifilter">
      <div class="html4strict geshifilter-html4strict">
        {% highlight javascript %}
<br/> 
<form> 
<input id="partnerData" /> 
<input id="nextButton" type="button" value="set partner data" onClick="changePData()"> 
</form> 
<script type = “text/javascript> 
function changePData() 
{ 
	var pData = document.getElementById("partnerData").value; 
	var flashObj = document.getElementById("kcw"); 
	flashObj.setPartnerData(pData); 
} 
</script>
{% endhighlight %}
      </div>
    </div>
  </li>
</ul>

## <a name="implement"></a>Implementing External Control on Flash Object Steps

When passing dynamic partner data to the KCW widget, it may raise a workflow need to change/control the internal steps of the KCW widget. This may be needed in order to set the additional partner data before media entry is created on the Kaltura system for the uploaded file.  
Therefore you need to allow end-users to upload their content only after they chose a site-specific filter related to it.  
It is possible to externally control KCW steps, using the following KCW public methods and JavaScript events:

<table>
  <thead>
    <tr>
      <th>
        Method signature
      </th>
      
      <th>
        Description
      </th>
      
      <th>
        JS Enabled
      </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>
        <span class="geshifilter"><code class="geshifilter-javascript">goNextStep&lt;span>(&lt;/span>&lt;span>)&lt;/span>&lt;span>:&lt;/span>&lt;span>void&lt;/span></code></span>
      </td>
      
      <td style="text-align: left;">
        Changes the kcw import state to the next one
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
    
    <tr>
      <td>
        <span class="geshifilter"><code class="geshifilter-javascript">goPrevStep&lt;span>(&lt;/span>&lt;span>)&lt;/span>&lt;span>:&lt;/span>&lt;span>void&lt;/span></code></span>
      </td>
      
      <td style="text-align: left;">
        Changes the kcw import state to the previous one
      </td>
      
      <td style="text-align: left;">
        Yes
      </td>
    </tr>
  </tbody>
</table>

The following example suggests a way to override the functionality of KCW widget’s “back” and “upload/next” built-in buttons and to externally control its internal steps. Combining such an implementation along with hiding the built-in control buttons of the KCW widget (using overlapping div) can enable site-specific workflow while relating dynamic data to uploaded content.

<div class="geshifilter">
  <div class="html4strict geshifilter-html4strict">
    {% highlight javascript %}
<!--implement advanced partner data communication functionality--> 
<br/> 
<form> 
<input id="backButton" type="button" value="Back" onClick="back()"> 
<input id="nextButton" type="button" value="Next" onClick="next()"> 
</form> 
<script type="text/javascript"> 
function next() 
{ 
	var flashObj = document.getElementById("kcw"); 
	flashObj.goNextStep(); 
} 
function back() 
{ 
	var flashObj = document.getElementById("kcw"); 
	flashObj.gobackStep(); 
} 
function nextButtonChanged(label, isEnabled, visible) 
{ 
	var nextButton = document.getElementById("nextButton"); 
	setButtonMode(nextButton, isEnabled, label) ;
} 
function backButtonChanged(label, isEnabled, visible) 
{ 
	var backButton = document.getElementById("backButton"); 
	setButtonMode(backButton, isEnabled, label);
} 
function setButtonMode(buttonObj, isEnabled, label) 
{ 
	buttonObj.disabled = !isEnabled; 
	buttonObj.value = label; 
} 
function kcwPendingChangeHandler(pending) 
{ 
	document.getElementById("nextButton").disabled = pending ? true : false; 
	document.getElementById("backButton").disabled = pending ? true : false; 
} 
</script>
{% endhighlight %}
  </div>
</div>

For further problem solving and details please refer to the <a href="http://knowledge.kaltura.com/search/KCW" class="bb-url">Frequently Asked Questions on the KCW Integration</a> guide.
