---
layout: page
title: "What is Tremor Media's added functionality"
date: 2012-01-18 10:55:18
---

<span style="font-size: small;">The following lists functionality that has been added to the Tremor plugin.</span>

<table border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td valign="top" width="114">
        <p class="TableHeading" style="text-align: left;">
          <strong><span style="font-size: small;">Functionality</span></strong>
        </p>
      </td>
      
      <td valign="top" width="167">
        <p class="TableHeading" style="text-align: left;">
          <strong><span style="font-size: small;">Description</span></strong>
        </p>
      </td>
      
      <td valign="top" width="308">
        <p class="TableHeading" style="text-align: left;">
          <strong><span style="font-size: small;">Example</span></strong>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="114">
        <p class="TableBodyText" style="text-align: left;">
          <span style="font-size: small;">Passing dynamic data</span>
        </p>
        
        <p class="TableBodyText">
          <span style="font-size: small;"> </span>
        </p>
      </td>
      
      <td valign="top" width="167">
        <p class="TableBodyText" style="text-align: left;">
          <span style="font-size: small;">By inserting specific key-value pairs in the uivars, a Kaltura partner can define that any Kaltura metadata gets passed to TremorMedia via the TremorMedia plugin. Then, using the Tremor ad server, the partner can decide how to target ads via the metadata.</span>
        </p>
        
        <p class="TableBodyText">
          <span style="font-size: small;">To enable this functionality, a custom ad path must be inserted into the uiconf.</span>
        </p>
        
        <p class="TableBodyText">
          <span style="font-size: small;"> </span>
        </p>
      </td>
      
      <td valign="top" width="308">
        <p class="TableCode" style="text-align: left;">
          <span style="font-size: small;">:  <var key="customAd.paramKey1" value="duration" />     <var key="customAd.paramValue1" value="{mediaProxy.entry.duration}" />     <var key="customAd.paramKey2" value="entryId" />     <var key="customAd.paramValue2" value="{mediaProxy.entry.id}" />     <var key="customAd.paramKey3" value="categories" />     <var key="customAd.paramValue3" value="{mediaProxy.entry.categories}" />     <var key="customAd.paramKey4" value="ContentRating" />     <var key="customAd.paramValue4" value="{mediaProxy.entryMetadata.ContentRating}" />     <var key="requiredMetadataFields" value="true" /></span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">Note: The ContentRating custom data field, has a slightly different value from the rest of the metadata.</span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="114">
        <p style="text-align: left;">
          <span style="font-size: small;">Internal companion ads</span>
        </p>
        
        <p>
          <span style="font-size: small;"> </span>
        </p>
      </td>
      
      <td valign="top" width="167">
        <p style="text-align: left;">
          <span style="font-size: small;">The ability to insert a companion ad directly on the list part of the playlist.</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">The companion ad must be inserted as a custom ad path via the uiconf or via additional parameters and plugins.</span>
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          <span style="font-size: small;"> </span>
        </p>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="114">
        <p style="text-align: left;">
          <span style="font-size: small;">Capping ads</span>
        </p>
        
        <p>
          <span style="font-size: small;"> </span>
        </p>
      </td>
      
      <td valign="top" width="167">
        <p style="text-align: left;">
          <span style="font-size: small;">A Kaltura partner can cap ads via the KMC based on the creation date.</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">To configure the Tremor plugin with the startDateOffset, with the parameter key maxAge, add the following 2 attributes to the XML (if the file is maintained manually):</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">paramKey1="duration" paramValue1="{tremor.createdAtOffset}"</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">or the equivalent uivars/flashvars line</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">paramKey1=duration&paramValue1={tremor.createdAtOffset}</span>
        </p>
        
        <p style="text-align: left;">
          <span style="font-size: small;">This is based on the assumption that the Tremor xml node has the id  set to 'tremor '. If using a studio player the id would be 'customAd'.<strong></strong></span>
        </p>
      </td>
      
      <td valign="top" width="308">
        <p>
          <span style="font-size: small;"> </span>
        </p>
      </td>
    </tr>
  </tbody>
</table>

 