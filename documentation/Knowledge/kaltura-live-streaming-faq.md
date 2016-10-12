---
layout: page
title: "Kaltura Live Streaming FAQ"
date: 2014-04-03 21:30:41
---

[collapsed title="Why when enabling recording and live streaming, the stream grows into a really long stream ( instead of creating lots of clips )?"]A break in broadcast could mean your network or encoder is going or has gone down. Kaltura supports appending content to the same logical entry for that event, with the assumption that you will want all content broadcasted to a particular named event or entry to be grouped together. Because the new Kaltura live streaming platform can instantly provision new live named entries, it is best practice to do so for every named event you broadcast. This keeps your archive of broadcasted events organized and keeps clean metadata on a per event basis.  You can create distinct entry sub-clips from your live event as its progressing using the “clipping” interface.[/collapsed]

 

[collapsed title="What protocols does live streaming support?"]By default the live streaming profile streams to both HDS and HLS. Custom transcode profiles can inclue, HDS, HLS, DASH, SmothStreaming & RTMP broadcasts. Additionally multicast protocols can be used in internal delivery contexts.[/collapsed]

 

[collapsed title="How do I customize the live streaming transcode profile?"]Please open a Kaltura customer care support ticket with the customizations your requesting. We will then add these custom flavors to your account and build the custom profile. The custom profile can then be selected as you provision live stream.[/collapsed]

 

[collapsed title="Is Kaltura Live Streaming compatible with encoders other than Flash Media Live Encoder ?"]Yes. Keep in mind Flash Media Live Encoder auto-translates stream names of type 1\_n3f4i616\_%i to 1\_n3f4i616\_1, 1\_n3f4i616\_2 per given flavors being passedthrough. In other words you may need to use the named entry with indexes for the stream name, instead of the %i name that the KMC provides.[/collapsed]

 

[collapsed title="What encoder does Kaltura recommend? "]In general any RTMP compatible encoder should work with the kaltura live platfrom. Wowza maintains a list of enocders on their site, also see KC artilce here that outlines compatible encoders. [/collapsed]