---
layout: page
title: "How to generate dynamic embed code in the KMC?"
date: 2014-12-02 14:15:01
---

<div id="main-header">
  <div id="title-heading" class="pagetitle with-breadcrumbs">
    <p id="title-text" class="with-breadcrumbs">
      Dynamic embed is recommended for cases where you want to dynamically control run time configuration and or have more control over the embed call. This includes setting plugin overrides, and setup callbacks. This embed method allows us to manipulate the player using JavaScript listeners.
    </p>
  </div>
</div>

<div id="content" class="page view">
  <div id="main-content" class="wiki-content">
    <div class="contentLayout2">
      <div class="columnLayout single" data-layout="single">
        <div class="cell normal" data-type="normal">
          <div class="innerCell">
            <div>
              <strong>Dynamic embed</strong> has many benefits over object tag or Flash library rewrites:
            </div>
            
            <div>
              <ul>
                <li>
                  <strong>fast - </strong> does not have to wait for DOM ready to output the Flash or HTML5 player
                </li>
                <li>
                  <strong>clean - </strong> uses JSON embed config for Flashvars and params
                </li>
                <li>
                  <strong>dynamic -</strong> better supports dynamic HTML l5 and Flash embed methods, responsive web design, and CSS inheritance
                </li>
              </ul>
            </div>
            
            <div>
              <hr />
            </div>
            
            <p>
              <br /><span class="mce-procedure">To generate dynamic embed code</span>
            </p>
            
            <ol>
              <li>
                In the Kaltura Management Console, navigate to Content tab, then select the entry you want to embed.<br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/42992236/image2014-10-26%2022%3A5%3A51.png?version=1&modificationDate=1414355438075&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/42992236/image2014-10-26%2022%3A5%3A51.png?version=1&modificationDate=1414355438075&api=v2" data-linked-resource-id="43188395" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-10-26 22:5:51.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="42992236" data-linked-resource-container-version="3" /><br /><br />
              </li>
              <li>
                 Click the Preview & Embed link.<br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/42992236/image2014-10-26%2022%3A6%3A54.png?version=1&modificationDate=1414355438088&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/42992236/image2014-10-26%2022%3A6%3A54.png?version=1&modificationDate=1414355438088&api=v2" data-linked-resource-id="43188396" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-10-26 22:6:54.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="42992236" data-linked-resource-container-version="3" /><br /><br />
              </li>
              <li>
                 Click Show Advanced Options, then change the embed type to Dynamic Embed.<br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/42992236/image2014-10-26%2022%3A9%3A14.png?version=1&modificationDate=1414355438096&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/42992236/image2014-10-26%2022%3A9%3A14.png?version=1&modificationDate=1414355438096&api=v2" data-linked-resource-id="43188397" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-10-26 22:9:14.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="42992236" data-linked-resource-container-version="3" /><br /><br />
              </li>
              <li>
                Click the Copy button to copy the embed code to the clipboard and add the code to the source code of the specific webpage.<br /><br /><img class="confluence-embedded-image" src="https://kaltura.atlassian.net/wiki/download/attachments/42992236/image2014-10-26%2022%3A12%3A27.png?version=1&modificationDate=1414355438030&api=v2" border="0" height="250" data-image-src="/wiki/download/attachments/42992236/image2014-10-26%2022%3A12%3A27.png?version=1&modificationDate=1414355438030&api=v2" data-linked-resource-id="43188398" data-linked-resource-version="1" data-linked-resource-type="attachment" data-linked-resource-default-alias="image2014-10-26 22:12:27.png" data-base-url="https://kaltura.atlassian.net/wiki" data-linked-resource-container-id="42992236" data-linked-resource-container-version="3" />
              </li>
            </ol>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>