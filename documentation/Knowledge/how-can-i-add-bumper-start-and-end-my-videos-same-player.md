---
layout: page
title: "How can I add a bumper at the start and end of my videos on the same player?"
date: 2013-05-17 14:37:04
---

To add the same bumper entry on both pre and post content, in <span>Javascript or flashvars or the KMC UI, UIVars, </span>set both pre and post sequence to 1.

Use the following string to configure a different post bumper (in Flash):

Studio string:

postbumper.plugin=true&postbumper.width=630&postbumper.height=355&

&postbumper.lockUI=false&postbumper.playOnce=false&postbumper.path=bumperPlugin.swf&

postbumper.relativeTo=bumper&postbumper.includeInLayout=false&postbumper.bumperEntryID=ENTRYID&postbumper.postSequence=1&postbumper.position=before&postbumper.id=bumper2 

 