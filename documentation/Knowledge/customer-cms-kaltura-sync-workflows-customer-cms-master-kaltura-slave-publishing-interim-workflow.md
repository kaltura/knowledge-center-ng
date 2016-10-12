---
layout: page
title: "Customer CMS-Kaltura Sync Workflows - Customer CMS (Master)->Kaltura (Slave) Publishing (Interim Workflow)"
date: 2012-02-03 01:11:26
---

As detailed in the article about [Migrating Legacy Code][1] , this workflow process is only an interim solution to allow the Kaltura-powered player to be launched and serve customer videos, without being dependent on a full implementation of a Kaltura-powered workflow.   
Once a video producer completes creating an asset in the customer CMS which results in having a video flavor, thumbnails and metadata in place, a Kaltura entry can now be created and captions generated, allowing the website to load the Kaltura-powered player with the newly created entry id and have it play the video via Kaltura (*in parallel, additional flavors, not mandatory for web playback, will be generated. E.g. iPad, iPhone, lower bandwidths*).  
As the customer CMS will remain the master editing place, changes to metadata in the CMS will need to be reflected in Kaltura, to allow the Kaltura player to load any relevant metadata in and outside customer’s website.

 [1]: http://knowledge.kaltura.com/customer-cms-kaltura-sync-workflows-migrating-legacy-content

Optimally, the following will be done automatically once a customer CMS video object is created or modified, but the script is described here as a standalone script, just in case it has to be done manually.

 

**syncCMSObjectToKaltura** (CMS object) {

       Create a Kaltura API session;

       IF there is no entry id assigned to the CMS object yet THEN

<p style="padding-left: 30px;">
  // Reuse the method defined in previous phase
</p>

              New entryId = **generateKalturaEntry** (CMS object, Kaltura session);

              IF entry was created successfully THEN       

                     Assign entryId to CMS object;

<p style="padding-left: 30px;">
  Send an auto-captioning request using the new entryId and CMS video url
</p>

                     Report or log success;

              ELSE

                     Report or log error;

              END IF

       ELSE // An entry id is already assigned, we’re now checking if entry needs to be updated

              New entryLastUpdDate = **getEntryLastUpdateDate**(entryId, Kaltura session);

              IF the CMS object was modified after entryLastUpdDate THEN    

                     **updateKalturaEntry**(entryId, CMS object, Kaltura session token);

              END IF

       END IF

}

 

The above code uses the following reusable method:

 

**updateKalturaEntry** (entryId, CMS object, Kaltura session token) {

 

       IF CMS video flavor required for website playback is newer or different THEN

              // Customer replaced a video file

              **replaceKalturaEntrySourceFlavor**(entryId, flavor url);

<p style="padding-left: 30px;">
  Send an auto-captioning request using the entryId and new/modified CMS video url
</p>

       END IF;

 

       IF CMS thumbnail is newer or different THEN

              **replaceKalturaEntryThumbnail**(entryId, thumbnail url);

       END IF;

      

       IF CMS metadata is newer or different THEN

              **updateKalturaEntryMetadata**(entryId, CMS object);

       END IF;

 

       Update geo-blocking restrictions as needed;

}            

* The above 3 utility methods are too technical for pseudo-code and are provided as code.