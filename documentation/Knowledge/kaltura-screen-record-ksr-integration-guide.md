---
layout: page
title: "Kaltura: Screen Record (KSR) Integration Guide"
date: 2013-07-15 16:41:17
---

This article is intended for Kaltura customers, partners and community members that are familiar with Kaltura terminology.

This article applies to:

*   Kaltura Screen Record (Screencast-O-Matic) widget v1.0.44.
*   Kaltura Partner Service: 3.0 (aka api_v3)

## Conventions

A string in brackets [] represents a value.

Replace the string – including the brackets – with an actual value.

Example: Replace *[SERVICENAME]* with *syndicationFeed*

<table border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="198">
        <p class="TableHeading">
          <strong>Term</strong>
        </p>
      </td>
      
      <td valign="top" width="425">
        <p class="TableHeading">
          <strong>Definition</strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableText">
          SOM
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="425">
        <p class="TableText">
          Screencast-O-Matic
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="198">
        <p class="TableText">
          KSR
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="425">
        <p class="TableText">
          Kaltura Screen Record widget
        </p>
      </td>
    </tr>
  </tbody>
</table>

The following topics are described:

*   [Simple Example Script][1]
*   [Include Kaltura Library][2]
*   [Define Constants and Variables][3]
*   [Construct Kaltura Objects for Session Initiation][4]
*   [Java Detection][5]
*   [Include the KSR JS Library][6]
*   [Load the Widget][7]
*   [KalturaScreenRecord JS Library API][8]
*   [KSR JS Library API][9]
*   [Kaltura Options][10]
*   [Kaltura Screen Recorder - Recommended Browsers][11]

 [1]: #SimpleExample
 [2]: #Include_Kaltura
 [3]: #Define_Constants
 [4]: #Construct
 [5]: #java_detection
 [6]: #Include
 [7]: #Load
 [8]: #KalturaScreenRecord
 [9]: #KSR_JS_Library
 [10]: #options
 [11]: #browsers

## <a name="SimpleExample"></a>Simple Example Script

<pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;?php

// include Kaltura Client Library

require_once('php5/KalturaClient.php');

//define constants

define("KALTURA_PARTNER_ID", Your Kaltura Partner ID);

define("KALTURA_PARTNER_SERVICE_SECRET", " Your Kaltura Service Secret");

$uiconfId = a UiConf ID; // integer

$partnerUserId = "Id of user";

 

// prepare KS

$config = new KalturaConfiguration(KALTURA_PARTNER_ID);

$client = new KalturaClient($config);

$ks = $client-&gt;generateSession(KALTURA_PARTNER_SERVICE_SECRET, $partnerUserId, KalturaSessionType::USER, KALTURA_PARTNER_ID);

 

?&gt;

&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"

 

        "http://www.w3.org/TR/html4/loose.dtd"&gt;

&lt;html&gt;

 

&lt;head&gt;

    &lt;title&gt;&lt;/title&gt;

&lt;!-- include KSR JS code --&gt;

    &lt;script type="text/javascript" src=" http://www.kaltura.com/p/&lt;?php echo KALTURA_PARTNER_ID; ?&gt;/sp/&lt;?php echo KALTURA_PARTNER_ID; ?&gt;/ksr/uiconfId/&lt;?php echo $uiconfId; ?&gt; "&gt;&lt;/script&gt;

&lt;/head&gt;

 

&lt;body&gt;

    &lt;div id="msg"&gt;

            &lt;div id="startbutton"&gt;

           &lt;!-- the click event on the following button will load the applet --&gt;

                &lt;input type="button" onclick="initKsr()" value="Start" /&gt;

            &lt;/div&gt;

        &lt;/div&gt;

     &lt;/div&gt;

 

    &lt;script type="text/javascript"&gt;

    function initKsr()
    {
       kalturaScreenRecord.initKsr('&lt;?php echo      KALTURA_PARTNER_ID; ?&gt;', '&lt;?php echo $ks; ?&gt;');

       kalturaScreenRecord.startKsr('&lt;?php echo KALTURA_PARTNER_ID; ?&gt;', '&lt;?php echo $ks; ?&gt;', false);

    }

     // callback function that will be called by library before loading the widget
     // this function removes description and tags from UI
      function removeDescAndTags(objOptions)
        {

            console.log("object before change");

            console.log(objOptions);

            objOptions['kaltura.submit.description.enabled'] = false;

            objOptions['kaltura.submit.tags.enabled'] = false;

            console.log("object after change");

            console.log(objOptions);

            return objOptions;

        }

       

        // setting callback to override some kaltura options

        kalturaScreenRecord.setModifyKalturaOptionsCallback(removeDescAndTags);

 

        kalturaScreenRecord.UploadCompleteCallBack = function(entryId)

        {

            alert("Kaltura KSR uploadCompleteCallBack: created entry with ID ["+entryId+"]");

        }

 

    &lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;</pre>

## <a name="Include_Kaltura"></a>Include Kaltura Library

The KalturaClient.php script is part of the PHP Kaltura API Client Library being included to enable the use of Kaltura objects.

<pre class="brush: php;fontsize: 100; first-line: 1; ">// include Kaltura Client Library

require_once('php5/KalturaClient.php');</pre>

## <a name="Define_Constants"></a>Define Constants and Variables

In the following example, the PHP code defines 2 constants and 2 variables, later to be used within implementation.

<pre class="brush: php;fontsize: 100; first-line: 1; ">//define constants

define("KALTURA_PARTNER_ID", Your Kaltura Partner ID);

define("KALTURA_PARTNER_SERVICE_SECRET", " Your Kaltura Service Secret");

$uiconfId = a UiConf ID; // integer

$partnerUserId = "ANONYMOUS";</pre>

The following lists the constants and variable parameters and their descriptions.

<table style="width: 640px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="240">
        <p class="TableHeading">
          <strong>Parameter</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="82">
        <p class="TableHeading">
          <strong>Data Type</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableHeading">
          <strong>Default Value</strong>
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="201">
        <p class="TableHeading">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="240">
        <p class="TableBodyText">
          KALTURA_PARTNER_ID          
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="82">
        <p class="TableBodyText">
          Numeric
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          N/A
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="201">
        <p class="TableBodyText">
          Enter your Partner ID. Please refer to <a href="http://knowledge.kaltura.com/node/162" target="_blank">Kaltura API Usage Guidelines</a>.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="240">
        <p class="TableBodyText">
          KALTURA_PARTNER_SERVICE_SECRET
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="82">
        <p class="TableBodyText">
          String
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          N/A
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="201">
        <p class="TableBodyText">
          Enter your Web Service Secret. Refer to the <a href="http://knowledge.kaltura.com/node/162" target="_blank">Kaltura API Usage Guidelines</a> for more information. The Secret string is used within Kaltura objects to create a secured session ID, preventing hacking and abuse attempts aiming to damage Partner/end-user’s content.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="240">
        <p class="TableBodyText">
          uiconfId
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="82">
        <p class="TableBodyText">
          Numeric
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          N/A
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="201">
        <p class="TableBodyText">
          Enter a uiconf ID that defines the KSR widget you want.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="240">
        <p class="TableBodyText">
          partnerUserID               
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="82">
        <p class="TableBodyText">
          String
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="118">
        <p class="TableBodyText">
          "ANONYMOUS"           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="201">
        <p class="TableBodyText">
          Use to populate your internal system end-user identifier. This variable is used to relate the uploaded content to its uploading user, and be used by Kaltura partners for user management and statistics tracking.
        </p>
      </td>
    </tr>
  </tbody>
</table>

## <a name="Construct"></a>Construct Kaltura Objects for Session Initiation

In the following example, the PHP code constructs the relevant Kaltura objects that are used for session initiation. The objects are constructed as defined and implemented in the relevant Kaltura API Client Library.

<pre class="brush: php;fontsize: 100; first-line: 1; ">// prepare KS

$config = new KalturaConfiguration(KALTURA_PARTNER_ID);

$client = new KalturaClient($config);

$ks = $client-&gt;generateSession(KALTURA_PARTNER_SERVICE_SECRET, $partnerUserId, KalturaSessionType::USER, KALTURA_PARTNER_ID);</pre>

The $ks variable will be passed through JS to the KSR applet.

## <a name="java_detection"></a>JAVA Detection

It is always advisable to have the latest version of JAVA installed on your machine.

The following should detect the JAVA version installed:

<pre class="brush: php;fontsize: 100; first-line: 1; ">function detectResult(Res)
    {
        Console.log(Res)
    }
kalturaScreenRecord.detectIfJavaEnabled(detectResult);
</pre>

## <a name="Include"></a>Include the KSR JS Library

The following script tag will include the KSR JS library in your page so you are able to load the widget.

<pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;script type="text/javascript" src=" http://www.kaltura.com/p/&lt;?php echo KALTURA_PARTNER_ID; ?&gt;/sp/&lt;?php echo KALTURA_PARTNER_ID; ?&gt;/ksr/uiconfId/&lt;?php echo $uiconfId; ?&gt; "&gt;&lt;/script&gt;</pre>

Replace the Kaltura URL ([www.kaltura.com][12]) in case you are working with an On-Prem/CE version of Kaltura.

 [12]: http://www.kaltura.com/

## <a name="Load"></a>Load the widget

<p class="Note">
  In this example we added a button in the page with an ‘onclick’ event. Clicking the button loads the widget by calling kalturaScreenRecord.startKsr function.
</p>

<pre class="brush: as3;fontsize: 100; first-line: 1; ">&lt;input type="button" onclick="kalturaScreenRecord.startKsr(&lt;?php echo KALTURA_PARTNER_ID;?&gt;, '&lt;?php echo $ks; ?&gt;', false);" value="Start" /&gt;</pre>

 The startKsr function expects 3 parameters:

*   Partner ID – in this sample we use the constant defined in php.
*   KS – a Kaltura session token
*   Detect – Boolean (true/false) to specify if you want to perform Java detection in the browser before loading the widget.
    *   This parameter is currently disabled, so passing “true” will not load the detection process.

## <a name="KalturaScreenRecord"></a>KalturaScreenRecord JS Library API

The KSR JS library exposes API that can be used in the page to change different settings or overriding methods.

In the example script that follows, the following two actions are implmented:

*   Override the UploadCompleteCallback function
*   Register a callback function to change Kaltura options before the widget is loaded.

<pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;script type="text/javascript"&gt;

        // callback function that will be called by library before loading the widget

        // this function removes description and tags from UI

        function removeDescAndTags(objOptions)

        {

            console.log("object before change");

            console.log(objOptions);

            objOptions['kaltura.submit.description.enabled'] = false;

            objOptions['kaltura.submit.tags.enabled'] = false;

            console.log("object after change");

            console.log(objOptions);

            return objOptions;

        }

       

        // setting callback to override some kaltura options

        kalturaScreenRecord.setModifyKalturaOptionsCallback(removeDescAndTags);

 

        kalturaScreenRecord.UploadCompleteCallBack = function(entryId)

        {

            alert("Kaltura KSR uploadCompleteCallBack: created entry with ID ["+entryId+"]");

        }

 

    &lt;/script&gt;</pre>

# <a name="KSR_JS_Library"></a>KSR JS Library API

## API Functions

The following lists all of the functions on kalturaScreenRecord object that you can call from your page.

<table style="width: 608px;" border="1" cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td valign="top" width="383">
        <p class="TableHeading">
          <strong>Function Call</strong>
        </p>
      </td>
      
      <td valign="top" width="225">
        <p class="TableHeading">
          <strong>Description             </strong>
        </p>
      </td>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setDetectTextJavaDisabled (txt);
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set the text that would appear/returned if detected that Java is disabled in your browser.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setDetectTextmacLionNeedsInstall (txt);
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set the text that would appear/returned if detected Mac Lion which requires Java to be installed
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setDetectTextjavaNotDetected(txt)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          The text that would appear/returned if Java was not detected.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setDetectResultErrorCustomCallback(funcName)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set a custom callback function name to be called if Java was not detected.
        </p>
        
        <p class="TableBodyText">
          If defined, this function will be called and other functionality overrideen.There will be no error message displayed.
        </p>
        
        <p class="TableBodyText">
          The function should expect a single string parameter with the keyword-description of the error.
        </p>
        
        <p class="TableBodyText">
          Available keywords: javaDisabled, macLionNeedsInstall, javaNotDetected
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setDetectResultErrorMessageElementId(id)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set the ID of a DOM element in your page where the error message would appear if Java is not detected.
        </p>
        
        <p class="TableBodyText">
          It's inner HTML will be set to the error message.
        </p>
        
        <p class="TableBodyText">
          The error messages can be defined using the setDetectText* functions, or simply use the default.
        </p>
        
        <p class="TableBodyText">
          If this fucntion is not defined and callback is not defined, an error will be written to console.log
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setDetectResultErrorMacLionNeedsInstallDomId(id)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set the ID of a DOM element in your page where an iframe with Mac Lion installation instructions will appear.
        </p>
        
        <p class="TableBodyText">
          The default DOM element is:
        </p>
        
        <p class="TableBodyText">
          <div id="macLionInstall" style="border: 1px solid black;  margin:18px 0; width:190px; height:40px;"></div>
        </p>
        
        <p class="TableBodyText">
          If you override using setDetectTextmacLionNeedsInstall(),  make sure you set the DOM ID using setDetectResultErrorMacLionNeedsInstallDomId() to an existing DOM element in your page.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setModifyJarsCallback (funcName)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set a callback function name/function that would change the list of jars before loading the KSR widget.
        </p>
        
        <p class="TableBodyText">
          Your function would get the list of jars (array) that are about to be loaded so you can modify them, and is expected to return an array of jars.
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="383">
        <p class="TableBodyText">
          kalturaScreenRecord.setModifyKalturaOptionsCallback(funcName)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="225">
        <p class="TableBodyText">
          Set a callback function name/function that would change Kaltura options before loading the KSR widget.
        </p>
        
        <p class="TableBodyText">
          Your function would get an object, with all Kaltura options, that are about to be loaded so you can modify them, and is expected to return a modified object.
        </p>
        
        <p class="TableBodyText">
          See <a href="#options">Kaltura Options</a>.
        </p>
        
        <p class="TableBodyText">
          Notice that options are wrapped with quotes, so you should access them as:
        </p>
        
        <p class="TableBodyText">
          yourVarName['option.name']
        </p>
        
        <p class="TableBodyText">
          and NOT as
        </p>
        
        <p class="TableBodyText">
          yourVarName.option.name - THIS WILL NOT WORK.
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Overridable Functions

The following lists all the functions of the kalturaScreenRecord object that you can override in your page to achieve different functionality.

<table style="width: 608px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="365">
        <p class="TableHeading" style="text-align: left;">
          <strong>Function Call</strong>
        </p>
      </td>
      
      <td valign="top" width="235">
        <p class="TableHeading" style="text-align: left;">
          <strong>Description</strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="365">
        <p class="TableBodyText">
          kalturaScreenRecord.onExitCallBack = function()
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="235">
        <p class="TableBodyText">
          default exit callback - does nothing
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="365">
        <p class="TableBodyText">
          kalturaScreenRecord.downloadCallBack = function(percent)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="235">
        <p class="TableBodyText">
          default download callback - writes to the console
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="365">
        <p class="TableBodyText">
          kalturaScreenRecord.logCaptureCallBack = function(phase, arg1, arg2
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="235">
        <p class="TableBodyText">
          default logCapture callback - writes to the console
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="365">
        <p class="TableBodyText">
          kalturaScreenRecord.startCallBack = function(result)
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="235">
        <p class="TableBodyText">
          default start callback - writes to the console
        </p>
      </td>
    </tr>
    
    <tr>
      <td style="text-align: left;" valign="top" width="365">
        <p class="TableBodyText">
          kalturaScreenRecord.UploadCompleteCallBack = function(entryId)
        </p>
        
        <p class="TableBodyText">
           
        </p>
      </td>
      
      <td style="text-align: left;" valign="top" width="235">
        <p class="TableBodyText">
          default upload-complete callback - writes to the console.
        </p>
      </td>
    </tr>
  </tbody>
</table>

# <a name="options"></a>Kaltura Options

The following lists the Kaltura-related options that you can change before loading the widget:

kaltura.server – the Kaltura URL in which the entry will be created

kaltura.partnerId – the partner ID

kaltura.session – the KS

kaltura.videoBitRate – bitrate for the captured video

kaltura.category – category to which the entry will be assigned

kaltura.conversionProfileId – conversion profile ID to apply on the entry

kaltura.submit.title.value – default entry title

kaltura.submit.description.value – default entry description

kaltura.submit.tags.value – default entry tags

kaltura.submit.title.enabled – whether “title” field is enabled in the UI

kaltura.submit.description.enabled - whether “description” field is enabled in the UI

kaltura.submit.tags.enabled - whether “tags” field is enabled in the UI

<p class="mce-heading-3">
  <a name="browsers"></a>Recommended Browsers and Operating Systems
</p>

 For a list of Kaltura supported browsers and operating systems see [Troubleshooting the Kaltura Screen Recorder][13].

 [13]: http://knowledge.kaltura.com/node/710/#recommended_browsers

<h3 class="mce-heading-3">
  <a name="mobile"></a>
</h3>