---
layout: page
title: "Kaltura Interactive Video Quizzes Release Notes"
date: 2016-02-14 01:29:13
---

<h3>
    Version 5.40.11
  </h3>
  
  <p>
    [collapsed title="Software Requirements"]
  </p>
  
  <h4>
    <strong>SW Components</strong>
  </h4>
  
  <p>
    The following are the minimum software requirements for IVQ to operate:
  </p>
  
  <ul>
    <li>
      KMS/KAF – 5.40.11  – SaaS customers will automatically be upgraded to this version.
    </li>
    <li>
      Quiz Creator/KEA (Kaltura Editing Application) – 1.0 – SaaS customers will automatically get this version.
    </li>
    <li>
      Player – The Quiz player (ID can be found in Quiz module) should be version 2.40 or later. This applies to all players across the application.
    </li>
  </ul>
  
  <p>
    Updating the Player version is done through the Player Studio (See the <a href="http://knowledge.kaltura.com/node/1148#upgrade" target="_blank">Universal Studio Information Guide</a> for more information) or in some cases through the KMS admin.
  </p>
  
  <p>
    <a href="#top">Back to top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Using IVQ in Channel Playlists"]
  </p>
  
  <h3>
    Using IVQ in Channel Playlists
  </h3>
  
  <p>
    KMS/KAF instances that use Channel Playlists must be configured by the KMS/KAF admin.
  </p>
  
  <p class="mce-procedure">
    To use IVQ in channel playlists
  </p>
  
  <ol>
    <li>
      Go to playlistPage module.
    </li>
    <li>
      Delete the uiconf and click Save.
    </li>
    <li>
      Press the Create button in the module page. This will initiate a new player deployment with the correct supported version.
    </li>
  </ol>
  
  <p>
    <a href="#top">Back to top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Using Exisiting Players with IVQ "]
  </p>
  
  <h3>
    Using Existing Players with IVQ
  </h3>
  
  <p>
    If you choose to use an existing player ID (must be version 2.40 or later)  for the IVQ (and not one that was automatically created after you enabled the Q<em>uiz</em> module) make sure you also include the following plugins to the player you selected in the Player Studio:
  </p>
  
  <ul>
    <li>
      For the playback player (found under Q<em>uiz</em> module, in <em>quizPlayerId</em> field), add:
    </li>
  </ul>
  
  <p style="padding-left: 60px;">
    "quiz": {
  </p>
  
  <p style="padding-left: 60px;">
          "plugin": true
  </p>
  
  <p style="padding-left: 60px;">
    }
  </p>
  
  <ul>
    <li>
      For the quiz editor player (under W<em>idgets</em> module, in <em>keaPlayerId</em> field) it is advised to keep the default player but you can also do the following:
    </li>
  </ul>
  
  <p style="padding-left: 60px;">
    Make sure the player you use in the editor has the following configuration:
  </p>
  
  <p style="padding-left: 60px;">
    "customButton": {<br />     "plugin": true<br /> }
  </p>
  
  <p style="padding-left: 60px;">
    and also:
  </p>
  
  <p style="padding-left: 60px;">
    "largePlayBtn": {
  </p>
  
  <p style="padding-left: 60px;">
     "plugin": false
  </p>
  
  <p style="padding-left: 60px;">
    },
  </p>
  
  <p>
    Note: you can use your own existing player on just one of them.  
  </p>
  
  <p>
     
  </p>
  
  <p>
    <a href="#top">Back to top</a>
  </p>
  
  <p>
     
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Limitations"]
  </p>
  
  <h3>
     Limitations
  </h3>
  
  <table style="width: 630px;" border="0" cellspacing="0" cellpadding="0" align="left">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          <strong>Issue</strong>
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          <strong>Description</strong>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-10358
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          The writing indicator mark (|) appears inside the player in the MS Edge browser.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-10358
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          If you skipped some questions, the <em>Almost Done </em>screen appears letting you know there are some questions you still need to answer before submission. For quizzes created on a YouTube video, the video does not start to play from the beginning, after clicking on “OK, Got it" button in the <em>Almost Done </em>screen.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-10225
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          The writing indicator mark (|) isn't vertically centered in the MS Edge browser.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-9585
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          The screen blinks before the 'Welcome screen' for a quizzes created for YouTube videos.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-10374
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          There may be text color differences between Chrome & Firefox browsers.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-8764
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          There is no drag option on the right side of the first answer area to move a question’s location in the video.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-8462
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          If multiple questions are placed on the exact same time/location, only the first one is used.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-8280
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          The scrubber is enabled on 'welcome' screen when part of a Channel playlist
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          KMS-10843
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          Quizzes do not playback on the following entry types: live, webcast, video presentation
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          <span> </span>
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          Quizzes do not playback on iPhones.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
          <span>KMS-8667</span>
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          Placing the first question within 2 sec of the beggining of the video can cuase unexpected behavior.
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
           
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          Player Hover functionality is not supported with IVQ
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
           
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          Autoplay functionality is not supported with IVQ
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="143">
           
        </td>
        
        <td style="text-align: left;" valign="top" width="911">
          <span>Ads, preroll, bumper, mid-roll are not supported with IVQ</span>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
    <strong> </strong>
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
     
  </p>
  
  <p>
    <a href="#top">Back to top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Known Limitations for IVQ in KAF"]
  </p>
  
  <p>
     
  </p>
  
  <h3>
    Known Limitations for IVQ in KAF
  </h3>
  
  <table style="width: 630px;" border="0" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="195">
          <p>
            <strong>Issue</strong>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="645">
          <p>
            <strong>Desrciption</strong>
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="195">
          <p>
            KMS-9107
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="645">
          <p>
            The quiz preview does not appear in the BSE screen.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="195">
          <p>
            KMS-9178
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="645">
          <p>
            The Quiz display in small and medium size in BSE may not display properly.
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
    <a href="#top">Back to top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Known Limitations for Gradebook Integration with Canvas"]
  </p>
  
  <h3>
    <strong>Known Limitations for Gradebook Integration with Canvas</strong>
  </h3>
  
  <ul>
    <li>
      When adding IVQ as an external app in Canvas to create an IVQ assignment with gradebook automation, you cannot embed Kaltura content in the rich-text editor in the same assignment.
    </li>
  </ul>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Known Issues"]
  </p>
  
  <p>
     
  </p>
  
  <h3>
    <strong>Known Issues </strong>
  </h3>
  
  <table style="width: 630px;" border="0" cellspacing="0" cellpadding="0">
    <tbody>
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10449<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            When in a quiz is defined with the Share option, the close window "X" button is missing. Clicking on play disables the Share
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10450<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            The close window "X" button is missing when opening and closing the info plugin before starting a quiz and re-entering to the Info plugin.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10360<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            iOS Safari – The Quiz score is pixelated.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10359<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            MS Edge browser – The selected answer under the Continue button may have a thick shadow.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10116<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            A black screen appears for 1 second after clicking on the Why or Hint icons on Ipads.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10639<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            The Info\Download plugins (on the top black line) pop up for 1 sec when a quiz screen is displayed.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10691<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            In some cases you may have to click twice on the touch screen when in full screen mode on an iOS8 tablet.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10242<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            Hexagons on the player scrubber do not display well in IE.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10866<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            When using the Embed Channel playlist option, the quiz's GUI is cut-off.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10860<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            When in channel playlists, switching between an image entry to an audio entry causes erroneous playback.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10415<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            A quiz answer may be partially hidden in the quiz screen when reviewing a submitted quiz.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10451<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            When opening a link in a new tab from the Share link, the quiz may display improperly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10885<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            CaptureSpace: When an anonymous user chooses to switch between streams, the answered questions become unanswered. The saved answers per question are removed.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10892<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            After clicking Got it, the Info plugin is showing ‘Almost done’ text.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-9562<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            If and when you press ‘space’ at the same time a question is shown, the video may get stuck with disabled controls
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10895<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            After uploading media and clicking Edit Quiz, the word 'Quiz' is not appended to the entry's name.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10912<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            Channel playlist – Continuous Playback is not working properly when stitching between a Youtube entry to a video entry.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10278<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            In case a quiz contains identical questions, the download PDF downloads only one of the questions.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-9204<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            An error message is not displayed when the internet disconnects.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-8787<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            In some cases of text input, a scroll bar on the question balloon appears.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-8465<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            Inside the quiz editor, the browser's back button may not function properly.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10673<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            In the quiz editor, there is no ‘Drag' indication on the right side for the first answer.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-9299<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            You can save a question/answer with a tag <xxxxxxx> that includes a value only. HTML tags are not allowed.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-8274<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            The Volume control is not disabled when a quiz is running.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-9365<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            In a tablet webview there is no swipe for the TIP area in the quiz editor.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-8287<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            There is no ability to define more than one question in one cuepoint/timestamp.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10909<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            iPad: when dragging the input answer rectangle to an area outside of the designed area, the buttons expand.
          </p>
        </td>
      </tr>
      
      <tr>
        <td style="text-align: left;" valign="top" width="150">
          <p class="TableBodyText">
            KMS-10861<span style="text-decoration: underline;"></span>
          </p>
        </td>
        
        <td style="text-align: left;" valign="top" width="893">
          <p class="TableBodyText">
            A quiz entry is not shown inside a channel playlist that was embedded (and contains quiz entry).
          </p>
        </td>
      </tr>
    </tbody>
  </table>
  
  <p>
     
  </p>
  
  <p>
    <a href="#top">Back to top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Tested Browsers"]
  </p>
  
  <p>
     
  </p>
  
  <h4>
    Tested Browsers
  </h4>
  
  <p>
    The following platforms were tested for this release (recommended resolution 1024x768) for quiz creation, playback and analytics:
  </p>
  
  <ul>
    <li>
      Tablet, Android 5.0, Chrome
    </li>
    <li>
      Tablet, Android 6.0, Chrome
    </li>
    <li>
      iPad, iOS 9, Safari
    </li>
    <li>
      iPad, iOS 8, Safari
    </li>
    <li>
      PC, Win10, IE11
    </li>
    <li>
      PC, Win 10, Chrome
    </li>
    <li>
      PC, Win 10, FireFfox
    </li>
    <li>
      Mac, El Capitan, Safari
    </li>
  </ul>
  
  <p>
    <strong><a href="#top"><br /></a></strong><a href="#top">Back to top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    <strong> </strong>
  </p>