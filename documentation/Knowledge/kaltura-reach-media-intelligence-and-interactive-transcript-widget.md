---
layout: page
title: "Kaltura REACH Media Intelligence and Interactive Transcript Widget"
date: 2016-03-27 07:07:26
---

<p>
    The transcription services REACH includes are media data (timed transcripts) intelligence, (topics, keywords, adwords)  to enhance your content ROI by powering content discovery, engagement, ad targeting, and asset management.
  </p>
  
  <p>
    In addition, REACH has an interactive transcript widget leveraging REACH proprietary media data available for select integrations. The functionality include the ability to search within videos as well as:
  </p>
  
  <ul>
    <li>
      Interactive transcript experience. The transcript is time stamped and synchronized to the video frame.
    </li>
    <li>
      Displays REACH media intelligence including topics, keywords and AdWords.
    </li>
    <li>
      Multi-language support for native captions and foreign language subtitles.
    </li>
    <li>
      Content search with heat map including words, topics, keywords, and entities.
    </li>
    <li>
      For videos with multiple speakers identified, speaker search by color coded heat map and time stamps.
    </li>
    <li>
      Complete customization including custom settings like social sharing, and transcript download.
    </li>
    <li>
      Configurable social sharing of selected videos down to the specific caption across sites like Facebook, Twitter and LinkedIn.
    </li>
    <li>
      Ability to download and print transcripts including speakers and time stamps.
    </li>
  </ul>
  
  <p>
     
  </p>
  
  <p>
    <a name="KMS_Setup"></a>
  </p>
  
  <p>
    [collapsed title="Using the REACH Interactive Transcript Widget Instructions for Captions in Kaltura MediaSpace"]
  </p>
  
  <div class="WordSection1">
    <p>
      For additional infromation see the REACH Interactive Transcription Widget and media data player for Kaltura MediaSpace data sheet <a href="http://knowledge.kaltura.com/sites/default/files/media%20player.pdf" target="_blank">here</a>
    </p>
    
    <ol>
      <li>
        <a href="http://knowledge.kaltura.com/universal-studio-information-guide#creating_a_player" target="_blank">Create or edit an existing player in the Universal Studio.</a>
      </li>
      <li>
        Click on the Plugin icon on the bottom left.
      </li>
      <li>
        Click Import Plugin.<br /><img src="../../assets/3081.img">
      </li>
      <li>
        Copy and insert the following string into the Plugin Configuration String box and click Import.<br /><code>onPageJs1=//mediadataplayer-cdn.cielo24.com/v2/stable/kaltura.js&cielo24Transcriptions.DynaTransWindowHeight=400&cielo24Transcriptions.DynaTransWindowTitle=MediaDataPlayer&cielo24Transcriptions.DynaTransClientLogo=https://mediadataplayer-cdn.cielo24.com/v2/stable/widget/img/logo-transparent.png&cielo24Transcriptions.DynaTransHideGear=FALSE&cielo24Transcriptions.DynaTransHideShare=FALSE&cielo24Transcriptions.DynaTransHidePrint=FALSE&cielo24Transcriptions.DynaTransHideDownload=FALSE&cielo24Transcriptions.DynaTransHideLeftMenu=FALSE&cielo24Transcriptions.DynaTransHideSpeakers=FALSE&cielo24Transcriptions.DynaTransHideTimestamps=TRUE&cielo24Transcriptions.DynaTransAutoscrollOff=FALSE&cielo24Transcriptions.DynaTransWidgetUrl=https://mediadataplayer-cdn.cielo24.com/v2/stable/widget/widget.html&cielo24Transcriptions.DynaTransHideMetaTopics=FALSE&cielo24Transcriptions.DynaTransHideMetaSpeakers=FALSE&cielo24Transcriptions.DynaTransHideMetaKeywords=FALSE&cielo24Transcriptions.DynaTransHideFooter=FALSE&cielo24Transcriptions.DynaTransEnableAdditionalCSS=TRUE&cielo24Transcriptions.DynaTranscriptStartsHidden=FALSE&cielo24Transcriptions.DynaTransAdditionalCSS=.action-edit #wrapper.video{margin-bottom:0}#mediaContainer #wrapper.video{height:auto;padding-bottom:0 !important;padding-top:0 !important;}#mediaContainer #wrapper.video #player div.kWidgetIframeContainer{position:relative;padding-bottom:56.25%;left:auto;top:auto}.entryTitle,.stat_data{margin-top:20px}#mediaContainer #wrapper.video #player div #cielo24-iframe-wrapper-kplayer{background:#FFF;height:auto;left:auto;position:relative;top:auto;width:auto}#mediaContainer #wrapper.video #player #cielo24-iframe-wrapper-kplayer iframe{background-color:#FFF;height:inherit;left:unset;position:unset;top:unset;width:none}</code>
      </li>
    </ol>
  </div>
  
  <div class="WordSection1">
    Under ‘UI variables’ you can now edit the values listed in the following table to customize the player display.<table style="width: 630px;" border="0" cellspacing="0" cellpadding="0" align="center">
      <tbody>
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              <strong>Variable</strong>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              <strong>Definition</strong>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              <strong>Default</strong>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              <strong>Default Meaning</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransWindowSize
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Size of Widget
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              400
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Sized at 400px.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransWindowTitle
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Name of Widget (Displayed in Footer)
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              Media Data Player
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Label displayed on widget.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransClientLogo
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Logo Displayed on right side of Footer
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              <a href="https://mediadataplayer-cdn.cielo24.com/v2/stable/widget/img/logo-transparent.png" target="_blank"><em><em>https://mediadataplayer-cdn.cielo24.com/v2/stable/widget/img/logo-transparent.png</em></em></a>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Logo link displayed on widget.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransClientHref
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Link for the 'client' logo displayed on left side of footer
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              <a href="https://cielo24.com/">https://cielo24.com</a>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Link displayed on left side of widget footer.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideGear
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Settings Gear (required for usability)
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Settings Gear is defaulted to display.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideShare
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Social Sharing icon
            </p>
            
            <p>
              Display
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Social Share is defaulted to display.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHidePrint
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Transcript Print icon Display
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Transcript Print icon is defaulted to display enabling printing of transcript.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideDownload
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Transcript Download icon Display
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Transcript Download icon is defaulted to display enabling download of text transcript.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideLeftMenu
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Tag icon to Display Media Intelligence (only when available for video)
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Tag icon defaulted to display media intelligence when the video contains media data. If there is no media data, the icon is dynamically hidden.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHide
            </p>
            
            <p>
              Speakers
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Default Display of Speaker Name Display within Interactive Transcript
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              The speaker name will only appear if speakers have been identified within the transcript. The setting configured is the default value for the display. This is also configurable via the Gear icon interactively.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideTimestamps
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Default Display of Timestamp Display per Speaker Change or Text Block
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              TRUE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Timestamps will only appear if speakers have been identified within the transcript. The setting configured is the default value for the display. This is also configurable via the Gear icon interactively.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransAutoscrollOff
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Default Behavior for Autoscroll of Interactive Transcript
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Autoscroll is the scrolling of the transcript with the playhead. The setting configured is the default value for the display. This is also configurable via the Gear icon interactively.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideMetaTopics
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Media Intelligence: Display Topics within 'Tags' icon
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              This configures the display capability. The Widget only displays the dropdown under the 'Tags' icon if a value is present in the video. On by default.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideMetaSpeakers
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Media Intelligence: Display Speakers within 'Tags' icon
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              This configures the 'capability' to display. The Widget only displays the dropdown under the 'Tags' icon if a value is present in the video. On by default.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideMetaKeywords
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Media Intelligence: Display Keywords within 'Tags' icon
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              This configures the 'capability' to display. The Widget only displays the  dropdown under the 'Tags' icon if a value is present in the video. On by default.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransTargetDivId
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Div name used to display widget in a target div for reference on web page
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              N/A
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Not used by default, only used if hosting on a web page to display the interactive transcript widgetin a particular location on the page. Value is 'div' name.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransAdditionalCSS
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Required for using interactive transcript widget in KMS
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
               
            </p>
            
            <p>
              .action-edit #wrapper.video{margin-bottom:0}#mediaContainer #wrapper.video{height:auto;padding-bottom:0 !important;padding-top:0 !important;}#mediaContainer #wrapper.video #player  div.kWidgetIframeContainer{position:relative;padding-bottom:56.25%;left:auto;top:auto}.entryTitle,.stat_data{margin-top:20px}#mediaContainer #wrapper.video #player div #cielo24-iframe-wrapper-kplayer{background:#FFF;height:auto;left:auto;position:relative;top:auto;width:auto}#mediaContainer #wrapper.video #player #cielo24-iframe-wrapper-kplayer iframe{background-color:#FFF;height:inherit;left:unset;position:unset;top:unset;width:none}
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Value only used if EnableAdditionalCSS is set to true. Required to display widget in KMS.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransEnableAdditionalCSS
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Required 'True' for use of interactive transcript widget within KMS
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p class="Tablebodytext">
              TRUE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Value determines if AdditionalCSS is referenced. Only used in KMS rendering, compatible with KMC.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransSearchVar
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              To pass search term as a parameter intointeractive transcript widget
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              N/A
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              Variable not set by default. Default name is 'cielo24search' to override set value for key variable.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransScroll bar
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Value for Scrollbar search result heat map display
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              N/A
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              By default vertical heatmap/scrollbar is displayed. To use horizontal heatmap for search results set value to
            </p>
            
            <p>
              'horizontal', omit for vertical only rendering.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransSponsorLogo
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              'Sponsor' logo on the right corner of the widget footer
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              cielo24 logo
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              No logo is present.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransSponsorHref
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Link for the 'Sponsor' logo displayed on right side of footer
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
               <em>cielo24Transcriptions.DynaTransSponsorHref</em>
            </p>
            
            <p>
              <a href="https://cielo24.com/"> </a>
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              No valid link.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTransHideFooter
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            <p>
              Controls display of the footer of the widget ­including all logos, links, and display text.
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            <p>
              FALSE
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            <p>
              By default, the footer will be displayed using Logos, Links, and Display Text defined.
            </p>
          </td>
        </tr>
        
        <tr>
          <td style="text-align: left;" valign="top" width="266">
            <p>
              cielo24Transcriptions.DynaTranscriptStartsHidden
            </p>
          </td>
          
          <td style="text-align: left;" valign="top" width="107">
            Transcript Panel Hidden
          </td>
          
          <td style="text-align: left;" valign="top" width="323">
            FALSE 
          </td>
          
          <td style="text-align: left;" valign="top" width="255">
            Variable controls whether the Interactive Transcript Panel is either shown or hidden by default.
          </td>
        </tr>
      </tbody>
    </table>
    
    <p>
      [/collapsed]
    </p>
    
    <p>
      [collapsed title="Using the REACH Interactive Transcript Widget Instructions for Captions in iFrame Embed"]
    </p>
    
    <p>
      The instructions for creating an iFrame supported version of the widget for embedding content is similar to the <a href="#KMS_Setup"><span>Mediaspace setup</span></a>. The value to copy into the ‘‘Plugin Configuration String’ is different:
    </p>
    
    <code class="brush: php;fontsize: 100; first-line: 1; ">IframeCustomPluginJs1=//mediadataplayer-cdn.cielo24.com/v2/stable/kaltura.js&cielo24Transcriptions.DynaTransWindowHeight=400&cielo24Transcriptions.DynaTransWindowTitle=MediaDataPlayer&cielo24Transcriptions.DynaTransClientLogo=https://mediadataplayer-cdn.cielo24.com/v2/stable/widget/img/logo-transparent.png&cielo24Transcriptions.DynaTransHideGear=FALSE&cielo24Transcriptions.DynaTransHideShare=FALSE&cielo24Transcriptions.DynaTransHidePrint=FALSE&cielo24Transcriptions.DynaTransHideDownload=FALSE&cielo24Transcriptions.DynaTransHideLeftMenu=FALSE&cielo24Transcriptions.DynaTransHideSpeakers=FALSE&cielo24Transcriptions.DynaTransHideTimestamps=TRUE&cielo24Transcriptions.DynaTransAutoscrollOff=FALSE&cielo24Transcriptions.DynaTransWidgetUrl=https://mediadataplayer-cdn.cielo24.com/v2/stable/widget/widget.html&cielo24Transcriptions.DynaTransHideMetaTopics=FALSE&cielo24Transcriptions.DynaTransHideMetaSpeakers=FALSE&cielo24Transcriptions.DynaTransHideMetaKeywords=FALSE&cielo24Transcriptions.DynaTransEnableAdditionalCSS=TRUE&cielo24Transcriptions.DynaTransHideFooter=FALSE&cielo24Transcriptions.DynaTransAdditionalCSS=.action-edit #wrapper.video{marginbottom:0}#mediaContainer#wrapper.video{height:auto;padding-bottom:0!important;padding-top:0!important}#mediaContainer#wrapper.video#playerdiv.kWidgetIframeContainer{position:relative;padding-bottom:56.25%;left:auto;top:auto}.entryTitle,.stat_data{margin-top:20px}#mediaContainer#wrapper.video#playerdiv#cielo24-iframe-wrapper-kplayer{background:#FFF;height:auto;left:auto;position:relative;top:auto;width:auto}#mediaContainer #wrapper.video #player #cielo24-iframe-wrapper-kplayeriframe{background-color:#FFF;height:inherit;left:unset;position:unset;top:unset;width:none}body{background-color:white}&onPageCss1=//mediadataplayer-cdn.cielo24.com/v2/stable/widget/css/kaltura/iframeEmbedOnPageStyle.css</code>
  </div>
  
  <div class="WordSection1">
     
  </div>
  
  <div class="WordSection1">
    To verify and ensure that the iFrame embed widget is configured correctly, review the following differences under the UI variables compared to the Mediaspace version of the widget:<p>
      ○    In the UI Variables, instead of <a href="#onPageJs1"><em>onPageJs1</em></a>, the key is <em>IframeCustomPluginJs1</em>
    </p>
    
    <p>
      ○    A new UI Variable, key ­<em>onPageCss1 </em>is set to the following value :
    </p>
    
    <p style="padding-left: 30px;">
      //<a href="http://mediadataplayer-cdn.cielo24.com/v2/stable/widget/css/kaltura/iframeEmbedOnPageStyle.css" target="_blank">mediadataplayer-cdn.cielo24.com/v2/stable/widget/css/kaltura/iframeEmbedOnPageStyle.css</a>
    </p>
    
    <p>
      ○  An additional style declaration body
    </p>
    
    <pre class="brush: php;fontsize: 100; first-line: 1; ">{background&shy;color:white</pre>
    
    <p>
      should be added to additionalCSS:
    </p>
    
    <pre class="brush: php;fontsize: 100; first-line: 1; ">.action-edit #wrapper.video{marginbottom:0}#mediaContainer#wrapper.video{height:auto;padding-bottom:0!important;padding-top:0!important}#mediaContainer#wrapper.video#playerdiv.kWidgetIframeContainer{position:relative;padding-bottom:56.25%;left:auto;top:auto}.entryTitle,.stat_data{margin-top:20px}#mediaContainer#wrapper.video#playerdiv#cielo24-iframe-wrapper-kplayer{background:#FFF;height:auto;left:auto;position:relative;top:auto;width:auto}#mediaContainer #wrapper.video #player #cielo24-iframe-wrapper-kplayeriframe{background-color:#FFF;height:inherit;left:unset;position:unset;top:unset;width:none}body{background-color:white}</pre>
    
    <p>
       
    </p>
    
    <p>
      To update the embed sizes for ‘browseandembed' (Mashup) or ‘embed’ functions either in the KAF as the default, or per embedded video to support the additional widget size (ex. 400px) configured for the interactive transcript player, add the widget height to sizes:
    </p>
    
    <ul>
      <li>
        Small: 304 x 595
      </li>
      <li>
        Medium: 400 x 650
      </li>
      <li>
        Large: 608 x 765
      </li>
    </ul>After setup, copy the embed code. Set the Embed Type to ‘iframe’ and check Support for 
    
    <em>HTTPS embed code.</em>
  </div>
  
  <div class="WordSection1">
    If you set the ‘embed' defaults in KAF,  the height will already be adjusted. If not, copy the iFrame embed code and manipulate it directly.<br /><img src="../../assets/3084.img">
  </div>
  
  <div class="WordSection1">
    <p>
      To have the height and width dynamic (responsive) within iFrame, adjust the code.
    </p>
    
    <p>
      By default, the embed code generated from Kaltura will look like this:
    </p>
  </div>
  
  <div class="WordSection1">
    <pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;iframe src="&lt;your link from generated embed code&gt;" width="560" height="395"
allowfullscreen webkitallowfullscreen mozAllowFullScreen frameborder="0"
style="width: 560px; height: 395px;" itemprop="video" itemscope
itemtype="http://schema.org/VideoObject"&gt;
&lt;span itemprop="name" content="Your title"&gt;&lt;/span&gt;
&lt;span itemprop="description" content="Your Description"&gt;&lt;/span&gt;
&lt;span itemprop="duration" content="189"&gt;&lt;/span&gt;&lt;span itemprop="thumbnail"
content="&lt;your link from generated embed code&gt;"&gt;&lt;/span&gt;
&lt;span itemprop="width" content="560"&gt;&lt;/span&gt;
&lt;span itemprop="height" content="395"&gt;&lt;/span&gt;
&lt;/iframe&gt;
</pre>
  </div>
  
  <div class="WordSection1">
    Update the embed code as follows:
  </div>
  
  <p class="WordSection1">
     
  </p>
  
  <pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;div style="position: relative; padding-bottom: 56.25%; height: 0; overflow:
hidden;"&gt;
&lt;div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"&gt;
&lt;div style="width: 100%; height: 100%;"&gt;&lt;iframe title="Your Title" src="&lt;your same link from generated embed code&gt;"
"width="100%" height="100%" 
allowfullscreen="allowfullscreen" webkitallowfullscreen="webkitallowfullscreen" mozallowfullscreen="mozallowfullscreen"&gt;&lt;/iframe&gt; 
&lt;/div&gt; 
&lt;/div&gt; 
&lt;/div&gt;</pre>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
     
  </p>