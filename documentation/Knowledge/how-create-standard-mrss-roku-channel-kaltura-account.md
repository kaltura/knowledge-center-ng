---
layout: page
title: "How to Create a Standard MRSS Roku Channel from a Kaltura Account "
date: 2012-09-07 01:01:50
---

Roku is a set-top box that allows you to stream content on your TV or connected device. Content is organized as a channel based user experience. For example, Netflix, Hulu Plus and Amazon Instant Video are prominent channels on the Roku. 

## Related Documentation & Resources

<span style="color: #3366ff;"><a href="http://knowledge.kaltura.com/node/661" target="_blank"><span style="color: #3366ff;">Roku MRSS Template Channel ReadMe</span></a> </span>

<span style="color: #3366ff;"><a href="http://knowledge.kaltura.com/node/657"><span style="color: #3366ff;">Roku Developer Guide</span></a></span>

<span style="color: #3366ff;"><a href="http://knowledge.kaltura.com/node/657"></a><a href="http://knowledge.kaltura.com/node/658" target="_blank"><span style="color: #3366ff;">Channelpackage</span></a></span>

<span style="color: #3366ff;"><a href="http://knowledge.kaltura.com/node/660" target="_blank"><span style="color: #3366ff;">Roku XSLT</span></a></span>

## Kaltura Supported Integration

Kaltura supports out of the box:

1.  Streaming the content via MRSS feed to the Roku
2.  The MRSS includes the following metadata that is displayed on the Roku:
<ol style="list-style-type: lower-alpha;">
  <li>
    Title
  </li>
  <li>
    Description
  </li>
  <li>
    Thumbnail
  </li>
  <li>
    Publication date
  </li>
  <li>
    Duration
  </li>
</ol>

### What is not supported in this integration?

1.  Monetization:<ol style="list-style-type: lower-alpha;">
      <li>
        PPV
      </li>
      <li>
        Subscriptions
      </li>
      <li>
        Advertising<br />Tremor supports advertising on the Roku and should be supported for a Kaltura customer that is also advertising with Tremor on the web to allow pre-roll advertisement on the Roku devices as well. 
      </li>
    </ol>

2.  Live streaming to the Roku device

## Setting Up a Channel

Since MRSS is not standardized, different vendors may expect different formats of MRSS. The Kaltura MRSS feed is not completely compliant with Roku.

The feed needs to be modified so that all fields can display properly on the Roku player. (see below).

### Terminology

XSL – XML fits in the requirements

XSLT – takes XML and changes the conditions, therefore transforming one XML into a different type of XML. 

<p class="mce-procedure">
  To create a Roku channel
</p>

1.  Choose the content of the channel (KMC)<ol style="list-style-type: lower-alpha;">
      <li>
        Make sure all entries have an MP4 flavor. The default flavor named “HQ MP4 for export” may serve for that purpose.
      </li>
      <li>
        You may use KMC built-in playlist mechanism to decide on the content.
      </li>
    </ol>

2.  Create the feed<ol style="list-style-type: lower-alpha;">
      <li>
        Copy and save the Roku XSLT that can be found <a href="http://knowledge.kaltura.com/node/660">here</a><span class="s1">. (Save it with an .xslt file extension).</span>
      </li>
      <li>
        Go to the KMC to Content>Syndication. Create a new feed.
      </li>
      <li>
        Choose what content you would like to be available in your feed (either all or a specific playlist).
      </li>
      <li>
        Next to Feed Type, choose Flexible Feed Format. Choose the Roku XSLT file, which is on saved on your desktop.
      </li>
    </ol>

3.  Prepare the package (windows explorer and a text editor)
<ol style="list-style-type: lower-alpha;">
  <li>
    Grab the bundle “ChannelForRokuDemo” and extract it.
  </li>
  <li>
    (optional) In the file ‘manifest’, you can change the name (‘title’) of the channel and its description (‘subtitle’).
  </li>
  <li>
    (optional)In the file ‘config.opml’ every ‘outline’ node represents a sub-channel. You can have one or more of these (nesting is also possible for further structure). <br /><ul>
      <li>
        For the feed URL, use the URL from before, only remove the partner ID section of it, so there is no ‘&’ symbol in it.
      </li>
      <li>
        Fill in the ‘title’, ‘subtitle’, ‘img’ (thumbnail) and ‘URL’ (feed URL) tags. for each subchannel.
      </li>
    </ul>
  </li>
  
  <li>
    Make sure that there are no other special characters (‘&<>) in any other field.
  </li>
  <li>
    Zip the package after you’re done with the changes.
  </li>
</ol>

4.  Create the package (command line & browser)
<ol style="list-style-type: lower-alpha;">
  <li>
    In the browser, go to the IP of the Roku player (can be taken from Roku player’s setting > player info).
  </li>
  <li>
    Browse and install the zip file created earlier.
  </li>
  <li>
    In command line :telnet[IP address on Roku] 8080
  </li>
  <li>
    Then type: genkey ; copy the password.
  </li>
  <li>
    Refresh the browser and go to ‘packager’ page.
  </li>
</ol>

5.  Publish the channel (Browser - Roku developer account)
<ol style="list-style-type: lower-alpha;">
  <li>
    Go to My Channels>Add private channel.
  </li>
  <li>
    Fill out relevant information, including providing two thumbnails, one SD and HD.<br /><ul>
      <li>
        The HD thumbnail should have dimensions of 290x218.
      </li>
      <li>
        The SD thumbnail should have dimensions of 214x144.
      </li>
      <li>
        Vanity access code: the customer can choose this. If the customer does not choose a vanity access code, a random code is created.
      </li>
    </ul>
  </li>
  
  <li>
    Insert the package that was downloaded before, click Save. Once the Publish arrow turns green, press it.<br /><br />
  </li>
</ol>

<h2 class="mce-procedure">
  To see the channel (as an end user)
</h2>

1.  Go to your Roku account  and add the private channel.
2.  Type in the vanity code and then approve adding the channel.

# Demo channel

Vanity code: <a href="https://owner.roku.com/add/KalRokDemoPrivate" target="_BLANK">KalRokDemoPrivate </a>