---
layout: page
title: "How to target information to an ad server?"
date: 2012-01-23 11:23:05
---

<span style="font-size: small;">While ads targeting is performed within the ad server, Kaltura’s VAST advertising module is designed to pass all the relevant targeting information to the ad server.</span>

<span style="font-size: small;">Targeting information can be set in several levels:</span>

*   <span style="font-size: small;">Targeting per player and ad slot – you can add additional key value pairs within the adtag URL. The ad server will use these for targeting.</span>
*   <span style="font-size: small;">Targeting per content item - The Kaltura VAST module supports dynamic pulling of metadata from the content item, and passes it to the ad server.</span>  
    <span style="font-size: small;"> For example for targeting a specific content category.</span>

<span class="mce-procedure" style="font-size: small;">To target information to the ad server</span>

1.  <span style="font-size: small;"><span style="font-size: small;">Drag content items into the category within the KMC.<br /></span></span>  
    <img src="../../assets/263">
    <span style="font-size: small;"><br /><br /></span>
2.  <span style="font-size: small;">Define the additional parameter in your ad server. </span>  
    <span style="font-size: small;"> For example in OpenX set the “category” parameter through “Site - Variable”</span><img src="../../assets/264">
3.  <span style="font-size: small;">Add category template category={mediaProxy.entry.categories} into the AdTag URL. At runtime this template will be populated with the actual values for each video played.</span>   
      
    <img src="../../assets/265">
      
    <span style="font-size: small;"> category={mediaProxy.entry.categories}</span>  
    <span style="font-size: small;"> tags={mediaProxy.entry.tags}</span>  
    <span style="font-size: small;"> name={mediaProxy.entry.name}</span>  
    <span style="font-size: small;"> id={mediaProxy.entry.id}</span>

 

 