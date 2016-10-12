---
layout: page
title: "Configuring the Tremor Media 3rd Party Ad Plugin"
date: 2012-01-18 13:30:21
---

<span style="font-size: small;">Tremor Media is an ad network that acts as a connector between ad companies/servers and their customers. Tremor Media connects with numerous ad sources and partners from a single control center and works with their customers to provide the appropriate ads from the appropriate ad servers.</span>

<p class="mce-procedure">
  <span style="font-size: small;"><span style="font-size: small;">To</span> configure the TremorMedia plugin</span>
</p>

> 1.  <span style="font-size: small;"><strong></strong>Go to your Tremor account; define ads, scheduling, targeting, etc. on the Tremor end.</span>
> 2.  <span style="font-size: small;"><strong></strong>Go to the Studio tab and edit an existing player or create a new one.</span>
> 3.  <span style="font-size: small;"><strong></strong>Select the Advertising tab.</span>
> 4.  <span style="font-size: small;"><strong></strong>Enable ads for the selected player.</span>
> 5.  <span style="font-size: small;"><strong></strong>Select Tremor as the Ad Source.</span><img src="../../assets/254">
> 6.  <span style="font-size: small;">In the key=value section, enter the policy ID. Type in progId=[policy ID].<br /><br /><span class="mce-note-graphic">NOTE: TremorMedia allows users to utilize other ad sources.</span></span><img src="../../assets/256">
> 
> <span class="mce-heading-1" style="font-size: small;">Tremor Media added functionality</span>
> 
> <span style="font-size: small;">The following lists functionality that has been added to the Tremor plugin.</span>
> 
> <table border="0" cellspacing="0" cellpadding="0">
>   <tbody>
>     <tr>
>       <td valign="top" width="114">
>         <p class="TableHeading" style="text-align: left;">
>           <span style="font-size: small;">Functionality</span>
>         </p>
>       </td>
>       
>       <td style="text-align: left;" valign="top" width="167">
>         <p class="TableHeading">
>           <span style="font-size: small;">Description</span>
>         </p>
>       </td>
>       
>       <td valign="top" width="308">
>         <p class="TableHeading" style="text-align: left;">
>           <span style="font-size: small;">Example</span>
>         </p>
>       </td>
>     </tr>
>     
>     <tr>
>       <td valign="top" width="114">
>         <p class="TableBodyText" style="text-align: left;">
>           <span style="font-size: small;">Passing dynamic data</span>
>         </p>
>       </td>
>       
>       <td style="text-align: left;" valign="top" width="167">
>         <p class="TableBodyText">
>           <span style="font-size: small;">By inserting specific key-value pairs in the uivars, a Kaltura partner can define that any Kaltura metadata gets passed to TremorMedia via the TremorMedia plugin. Then, using the Tremor ad server, the partner can decide how to target ads via the metadata.</span>
>         </p>
>         
>         <p class="TableBodyText">
>           <span style="font-size: small;">To enable this functionality, a custom ad path must be inserted into the uiconf.</span>
>         </p>
>         
>         <p class="TableBodyText">
>           <span style="font-size: small;"> </span>
>         </p>
>       </td>
>       
>       <td valign="top" width="308">
>         <p class="TableCode" style="text-align: left;">
>           <span style="font-size: small; font-family: courier new,courier;">:  <var key="customAd.paramKey1" value="duration" />     <var key="customAd.paramValue1" value="{mediaProxy.entry.duration}" />     <var key="customAd.paramKey2" value="entryId" />     <var key="customAd.paramValue2" value="{mediaProxy.entry.id}" />     <var key="customAd.paramKey3" value="categories" />     <var key="customAd.paramValue3" value="{mediaProxy.entry.categories}" />     <var key="customAd.paramKey4" value="ContentRating" />     <var key="customAd.paramValue4" value="{mediaProxy.entryMetadata.ContentRating}" />     <var key="requiredMetadataFields" value="true" /></span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small; font-family: courier new,courier;">Note: The ContentRating custom data field, has a slightly different value from the rest of the metadata.</span>
>         </p>
>       </td>
>     </tr>
>     
>     <tr align="left">
>       <td align="left">
>         <p style="text-align: left;">
>           <span style="font-size: small;">Internal companion ads</span><span style="font-size: small;"> </span>
>         </p>
>       </td>
>       
>       <td style="width: 167px;" align="left" valign="top">
>         <p style="text-align: left;">
>           <span style="font-size: small;">The ability to insert a companion ad directly on the list part of the playlist.</span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small;">The companion ad must be inserted as a custom ad path via the uiconf or via additional parameters and plugins.</span>
>         </p>
>       </td>
>       
>       <td valign="top" width="308">
>         <p>
>           <span style="font-size: small; font-family: courier new,courier;"> </span>
>         </p>
>       </td>
>     </tr>
>     
>     <tr>
>       <td valign="top" width="114">
>         <p style="text-align: left;">
>           <span style="font-size: small;">Capping ads</span>
>         </p>
>       </td>
>       
>       <td valign="top" width="167">
>         <p style="text-align: left;">
>           <span style="font-size: small;">A Kaltura partner can cap ads via the KMC based on the creation date.</span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small;">To configure the Tremor plugin with the startDateOffset, with the parameter key maxAge, add the following 2 attributes to the XML (if the file is maintained manually):</span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small; font-family: courier new,courier;">paramKey1="duration" paramValue1="{tremor.createdAtOffset}"</span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small; font-family: courier new,courier;">or the equivalent uivars/flashvars line</span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small; font-family: courier new,courier;">paramKey1=duration&paramValue1={tremor.createdAtOffset}</span>
>         </p>
>         
>         <p style="text-align: left;">
>           <span style="font-size: small;"><span style="font-family: courier new,courier;">This is based on the assumption that the Tremor xml node has the id  set to 'tremor '. If using a studio player the id would be 'customAd'.</span><strong></strong></span>
>         </p>
>       </td>
>       
>       <td valign="top" width="308">
>         <p>
>           <span style="font-family: courier new,courier;"> </span>
>         </p>
>       </td>
>     </tr>
>   </tbody>
> </table>