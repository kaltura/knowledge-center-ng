---
layout: page
title: "How to Start a Kaltura Session using the TestMe Console"
date: 2014-11-17 15:00:43
---

<span class="mce-procedure">To start a Kaltura Session</span>

1.  Go to: <a href="http://www.kaltura.com/api_v3/testme" class="external-link" rel="nofollow">http://www.kaltura.com/api_v3/testme</a>
2.  Select **Session** from the Select Service drop down list.  
    <img src="../../assets/3365">
      
      
    
3.  <span>Select </span>**Start**<span> from the Select action drop-down list.</span>  
    <span><img src="../../assets/3364">
    <span><br /></span>

At this point you need to log in to KMC and retrieve some information.

<p class="mce-procedure">
  To retreive information from the KMC
</p>

1.  <span>After logging in to KMC, click the </span>**Settings**<span> button and then </span>**Integration settings. **
2.  <span>Save the following information:(actual information is blurred intentionally)</span><ol style="list-style-type: lower-alpha;">
      <li>
        <strong>Partner ID.</strong>
      </li>
      <li>
        <strong>Administrator Secret.</strong><br /><strong>*The numbers and letters are different for each Partner.*</strong><strong><br /></strong><img src="../../assets/3369">
      </li>
    </ol>

3.  Return to the TestMe Console and paste all the Partner ID and Administrator Secret information and change the type field from **USER** to **ADMIN**.  
     <img src="../../assets/3366">
      
    
4.  After pressing send, you should see a code appear at the right side of screen, this is the KS, a Kaltura Session key.  
    <img src="../../assets/3367">
5.  At this point the KS field will autofill with the KS string.