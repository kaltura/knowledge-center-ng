---
layout: page
title: "Customer CMS-Kaltura Sync Workflows - Migrating Legacy Content"
date: 2012-02-03 01:17:12
---

The following method should be available as a standalone script and will probably not be used when switching to phase 2.

 

**bulkGenerateKalturaEntries** (filter1, filter2…) { // Allow filtering by creation date, section…

       Create a Kaltura API session token;

<p style="padding-left: 30px;">
  FOR EACH CMS object which fits filters 1, 2… and doesn’t yet have a Kaltura entryId DO {
</p>

              New entryId = **generateKalturaEntry** (CMS object, Kaltura session token);

              IF entry was created successfully THEN

                     Assign entryId to CMS object;

                     Send an auto-captioning request using the new entryId and CMS video url

                     Report or log success;

              ELSE

                     Report or log error;

              END IF

       }

}

The above code uses the following reusable method:

**generateKalturaEntry** (CMS object, Kaltura session token) { // Will be reused by sync workflow 2

       Create a new Kaltura entry container;

<p style="padding-left: 30px;">
  Create the entry’s flavors group based on the list of flavor urls in the CMS object;<br /> // In most customer cases this will be a single flavor
</p>

       Generate entry thumbnails using the list of thumbnail urls in the CMS object;

       Set entry’s metadata fields with corresponding values from the CMS object;

       Assign geo-blocking restrictions as needed;

       Return the new entry’s id;

}            