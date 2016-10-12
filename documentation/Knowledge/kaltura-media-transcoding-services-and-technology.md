---
layout: page
title: "Kaltura Media Transcoding Services and Technology"
date: 2015-05-11 16:01:47
---

<div id="main-header">
  <div id="title-heading" class="pagetitle with-breadcrumbs">
    <h1 id="title-text" class="with-breadcrumbs">
      <a name="top"></a>Kaltura Media Transcoding Services and Technology
    </h1>
  </div>
</div>

Kaltura Media Transcoding Services provides robust production grade cloud transcoding microservices and tools to manage seamless encoding workflows at any scale and quality requirements, for the web, broadcast, studio, or secure internal enterprise applications. Architected to handle any input type and file size over large volumes of jobs, Kaltura Media Transcoding Services handle any job from simple web delivery to complex production workflows converting any input format of uploaded video, audio, image and even documents into a variety of flavors (transcoded output renditions).

With Kaltura's infinitely scalable enterprise-grade Video Platform as a Service, our media transcoding services free you of the expense and hassle of maintaining your own transcoding hardware, tuning performance, and doing the guesswork of which architecture, encoder engines or settings work best for your input files, delivery networks or playback devices. We continuously monitor and optimize the transcoding cloud to support the latest formats and codecs, CDNs, encryption and delivery standards, ensuring your viewers always get the best video experience on any device.

True to Kaltura's Open and Interoperable values and API driven architecture, Kaltura Media Transcoding Services are consumable through robust set of microservices and the Kaltura API Client Libraries and SDKs, simplifying the creation of complex workflows alongside full control and extensibility through Kaltura's backend plugins mechanism.

Like the rest of the Kaltura Platform, the underlying technology of the Kaltura Media Transcoding Services was built to be deployed on any infrastructure, on premises or public cloud.  It is provided with provisioning, monitoring and detailed diagnostic tools as well as robust set of backend management APIs allowing cloud providers to run its own media transcoding services.

The following topics are described:

*   **[Ingest From Any Source -  Transcode For Any Target][1]**
*   **[The Kaltura Decision Layer][2]**
*   **[Media Encryption and Digital Rights Management (DRM)][3]**
*   **[Transcoding Prioritization][4]**
*   **[Transcoding Times and Quality of Service][5]**
*   **[][5][Programmatic Media Authoring API and Tools][6]**
*   **[Batch Architecture and Backend Plugins][7]**
*   [**Dedicated Transcoding**][8]

 [1]: #ingest
 [2]: #decision
 [3]: #drm
 [4]: #prioritization
 [5]: #qos
 [6]: #tools
 [7]: #plugins
 [8]: #dedicated

<h2 id="KalturaMediaTranscodingServicesandTechnology-IngestFromAnySource,TranscodeForAnyTarget">
  <a name="ingest"></a>Ingest From Any Source -  Transcode For Any Target
</h2>

New devices, cameras and input sources are introduced every month, from studio gear to webcam through conferencing and webcasting applications, to surveillance cameras and satellite feeds. The ever growing innovations in media bring challenges with new formats, codecs and standards that require constant monitoring of the industry shifts and continuous optimization of hardware, software and practices to ensure your users always get the best quality viewing experience. Kaltura Media Transcoding Services free you from these worries by providing always up to date transcoding services, optimized to the latest formats, codecs and standards.

<h3 id="KalturaMediaTranscodingServicesandTechnology-IntegratedEncodingEngines">
  Integrated Encoding Engines
</h3>

<p class="p1">
  <span class="s1">The following lists the various tools and encoding engines currently integrated and orchestrated (see: <a href="https://kaltura.atlassian.net/wiki/display/MPM/Kaltura+Media+Transcoding+Services+and+Technology#KalturaMediaTranscodingServicesandTechnology-decsionlayer">Kaltura Decision Layer</a>) in the Kaltura Media Transcoding Services:</span>
</p>

<li class="p1">
  <span class="s1">Common Video Encoding Engines: FFMPEG, Mencoder, VLC</span>
</li>
<li class="p1">
  <span class="s1">Proprietary Video Encoding/Encryption Engines: Microsoft Expression Encoder, QuickTimeTools, WebexNbrplayer, Widevine</span>
</li>
<li class="p1">
  <span class="s1">Video Segmentation and Delivery Optimization Engines: Mp4box, FastStart, Segmenter, ISM Index, ISM Manifest, SmilManifest, SmoothProtect </span>
</li>
<li class="p1">
  <span class="s1">Image Conversion: ImageMagick</span>
</li>
<li class="p1">
  <span class="s1">Document Conversion: PPT 2 Image, </span><span class="s1">PDF 2 SWF, PDF Creator</span>
</li>
<li class="p1">
  <span class="s1">Experimental Video Features: Third party encoders</span><span class="s1"><br /></span>
</li>
<li class="p1">
  <span class="s1">Deprecated or Legacy Video Encoders</span>
</li>

<p class="p1">
  <span class="s1">Each encoding engine is designated with the tasks it does best, and is optimized for quality, speed, reliability and cost-efficiency (saving on file size without compromising quality which in turn reduces publisher's costs on storage and bandwidth and delivers a superior viewing experience).  Engines are leveraged according to the source media, target media specs and expected delivery standard, some are often used as fall-back engines to each other according to the transcoding profile settings.<br /></span>
</p>

<h3 id="KalturaMediaTranscodingServicesandTechnology-CommonlyUsedVideoFormatsandCodecs">
  <strong>Commonly Used Video Formats and Codecs </strong>
</h3>

<p id="main-content" class="wiki-content">
  For a list of commonly used media formats and codecs that were tested and optimized for transcoding and delivery by Kaltura, see <a href="http://knowledge.kaltura.com/node/79" target="_blank">What are the supported Transcoding formats for the SaaS edition?</a> 
</p>

<p class="wiki-content">
  Additional codecs and formats are supported by the underlying encoder engines and can be ingested and transcoded by Kaltura. For further details and discovery regarding a specific codec or format that are not listed, please <a href="http://corp.kaltura.com/company/contact-us" class="external-link" rel="nofollow">contact us</a>.
</p>

<h4 id="KalturaMediaTranscodingServicesandTechnology-Ingest(Input)FileFormatsandCodecs">
  <a href="#top">Back to top.</a>
</h4>

<h2 id="KalturaMediaTranscodingServicesandTechnology-decsionlayerTheKalturaDecisionLayer">
  <span class="confluence-anchor-link"></span><a name="decision"></a>The Kaltura Decision Layer
</h2>

Kaltura transcoding workflows take the source file and transcoding profile (representing the list of the required flavors) as an input. The output is the transcoded videos as outlined in the transcoding profile. A flavor represents the set of parameters (format, codecs, bitrates, and other parameters such as video manipulation like trimming or scaling). The assets are generated to match the settings specified for each flavor in the transcoding profile.

The transcoding workflow is orchestrated by the "**Kaltura Decision Layer**" - a mechanism that optimizes the choice of encoder, parameters used and fail-over encoders for a given source media and desired output flavors.

These are the five stages of the transcoding process:

*   **[Analysis][9]** - Synopsis of the source media file
*   **[Intermediate-Source Processing][10]** - Pre-processing for non-standard media and handling of proprietary formats and codecs 
*   **[Optimization][11]** - Decision tree that optimizes for quality and efficiency
*   **[Asset Generation][12]** - Distributed batch transcoding of the source into each desired flavor
*   **[Validation][13]** - Testing and verification of generated flavors against source specifications and expected standards

 [9]: #analysis
 [10]: https://kaltura.atlassian.net/wiki/display/MPM/Kaltura+Media+Transcoding+Services+and+Technology#KalturaMediaTranscodingServicesandTechnology-intermediate
 [11]: #optimization
 [12]: #asset_generation
 [13]: #Validation

<h3 id="KalturaMediaTranscodingServicesandTechnology-analysisAnalysis" class="mce-heading-4">
  <span class="confluence-anchor-link"></span><a name="analysis"></a>Analysis
</h3>

The first step in the transcoding process is to analyze the source media characteristics and parameters. Based on the source parameters, the Kaltura Decision Layer decides whether there is a need for an intermediate-source processing phase. The transcoding logic then attempts to match the best encoding settings for that source and for the specific flavor in the transcoding profile specified. For example, in most cases, the bitrate and the frame size of the generated flavors should not exceed the source file bitrate and frame size. These decision settings can be overridden in the <a href="http://knowledge.kaltura.com/node/61" class="external-link" rel="nofollow">transcoding profile settings</a>.

<h3 id="KalturaMediaTranscodingServicesandTechnology-intermediateIntermediate-SourceProcessing">
  <span class="confluence-anchor-link"></span><a name="source_processing"></a>Intermediate-Source Processing
</h3>

With some proprietary formats and codecs, a dedicated hardware, operating system or software may be required to handle the transcoding of such files. In such cases Kaltura will leverage the dedicated technology to convert the ingested proprietary source into an intermediate-source (file of non-proprietary format/codec, usually MP4/H.264 or WMV) and then continue the processing as usual.

For example (read: <a href="http://knowledge.kaltura.com/node/723" class="external-link" rel="nofollow">Best Practices For Uploading Content Created Using Screencast Tools</a>):

*   Webex/ARF - <a href="http://www.webex.com/play-webex-recording.html" class="external-link" rel="nofollow">Cisco's WebEx Network Recording Tool</a> will be used to covert the proprietary WebEx format before continuing with the media transcoding process.
*   GoToMeeting Codec - Windows Expression Encoder 4 will be used to covert the proprietary GoToMeeting codec before continuing with the media transcoding process.
*   QuickTime Video (QT) - MAC machines will be used to covert the proprietary QT format before continuing with the media transcoding process.

In addition to processing 'special source formats', an intermediate-source is also used to handle known video issues, such as handling artifacts in Digital Video sources, adding silent audio tracks for assets that will be ciphered by Widevine DRM, and other cases.

<h3 id="KalturaMediaTranscodingServicesandTechnology-optimizationOptimization" class="mce-heading-4">
  <a name="optimization" rel="nofollow"></a><span class="confluence-anchor-link"></span>Optimization
</h3>

After analyzing all the flavors, the transcoding process begins to optimize the following aspects of the video transcoding:

*   Bitrate - To prevent generation of assets with similar/close bitrates and avoid reduction in quality and cost-efficiency.
*   Frame Size - There should be at least one flavor that will match the source frame size as closely as possible. For example: this is important for  "presentations style" videos that are of a low bitrate and large frame sizes. 
*   Delivery Types - There should be at least one flavor for every delivery type (Web, HLS, ...) to ensure smooth and reliable delivery.

The redundant flavors are marked as Non Applicable (i.e. output flavors that should not be created) for the next step, <span><a href="https://kaltura.atlassian.net/wiki/display/MPM/Kaltura+Media+Transcoding+Services+and+Technology#KalturaMediaTranscodingServicesandTechnology-assetgen">Asset Generation</a>.</span>

<h3 id="KalturaMediaTranscodingServicesandTechnology-assetgenAssetGeneration" class="mce-heading-4">
  <a name="asset_generation" rel="nofollow"></a><span class="confluence-anchor-link"></span>Asset Generation
</h3>

<a href="http://knowledge.kaltura.com/node/230" class="external-link" rel="nofollow">The Kaltura batch system</a> executes the asset generation. In this phase, each of the flavors specified in the transcoding profile will be executed as transcoding jobs in parallel and according to priority and resources availability by the designated encoder. In case of a specific transcoding tool failure, the batch worker attempts to use the rest of the fallback transcoders that are available for the specific flavor.

When an asset transcoding completed successfully, the newly transcoded asset goes into the validation phase.

<h3 id="KalturaMediaTranscodingServicesandTechnology-validationValidation" class="mce-heading-4">
  <a name="Validation" rel="nofollow"></a><span class="confluence-anchor-link"></span>Validation
</h3>

Based on the source and the flavors, the asset is checked for existence of the required content streams and the correct duration or any errors from the transcoder. If an asset has been found to be invalid or faulty, the next defined fall-back transcoding engine is used to re-try the conversion.

[Back to top.][14]

 [14]: #top

<h2 id="KalturaMediaTranscodingServicesandTechnology-MediaEncryptionandDigitalRightsManagement(DRM)">
  <a name="drm"></a>Media Encryption and Digital Rights Management (DRM)
</h2>

Protecting media content from unauthorized viewing and copying is often critical to video operations. Whether for public facing paid content or sensitive corporate videos, DRM (Digital Rights Management) offers controls needed to ensure media is used only as intended. Integrated and certified with Google Widevine (Setup guide) and Microsoft PlayReady DRM technologies for content protection, Kaltura Media Transcoding Services simplifies the management of multi-DRM solution and media encryption process as an integrated step of the Kaltura media ingestion and preparation workflow. 

[Back to top.][14]

<h2 id="KalturaMediaTranscodingServicesandTechnology-TranscodingPrioritization">
  <a name="prioritization"></a>Transcoding Prioritization
</h2>

Whether you're running a private small operation or large public transcoding cloud - Kaltura is built to provide the architecture that serves your needs from a low volume to millions of transcoding jobs daily.  With scale, and different deployment architectures, comes the need to control priority queues and even provide reserved instances. Kaltura Media Transcoding Services is built with multi-tenancy and quality of service management in mind.

<p class="p1">
  <span class="s1">The weighting of the different factors outlined here may be configured to maximize:</span>
</p>

<li class="p1">
  <span class="s1"><strong>Throughput</strong> - Maximize the speed at which transcoding jobs are completed and utilization of the available system resources. Here the most dominating factor is the video duration.</span>
</li>
<li class="p1">
  <span class="s1"><strong>Fairness</strong> - Balance the number of running jobs between publisher accounts in the Kaltura deployment and prevent "starvation" of accounts. In this algorithm the dominant factors are the number of currently running jobs per account and the Account Class of Service. </span>
</li>

<p class="p1">
  <span class="s1">The ratio between these two strategies is configurable per Kaltura deployment (100 = maximum throughput, 0 = maximum fairness).</span>
</p>

<h3 id="KalturaMediaTranscodingServicesandTechnology-VideoTranscodingJobsPrioritizationFactors" class="p1">
  <span class="s1">Video Transcoding Jobs Prioritization Factors</span>
</h3>

The job prioritization mechanism takes into account the following factors: (Note that each of the factors may be configured and tweaked for influence per Kaltura deployment)

1.  **The duration of the source video** - For the following reasons, transcoding jobs of shorter duration generally have a higher priority.
    *   The users expectations usually correlate to the video duration: a user who uploads a 5 min video generally expects the video to be ready in a matter of minutes, while a user who uploads an hour long video will expect it to take more time.
    *   The duration of a video provides a rough estimate for the execution time required to process the transcoding of that video.
2.  **Impact on "Entry Readiness"** - Transcoding of flavors that are marked as "required" as for the entry status to be READY, are assigned higher priority than flavors marked as "optional". If all flavors are marked as optional, the lowest bitrate flavor will implicitly be treated as required. (Read more on <a href="http://knowledge.kaltura.com/node/61" class="external-link" rel="nofollow">Entry Readiness settings</a>).
3.  **The ingestion / upload method** - Videos that were singularly ingested using the upload API (e.g. via browser or mobile app upload) will be assigned a higher priority than videos ingested as part of a bulk upload (<a href="http://knowledge.kaltura.com/node/49" class="external-link" rel="nofollow">using CSV / XML bulk upload</a>).
4.  **The ingesting account overhead** - As more transcoding jobs will be executed under a single account, the pending jobs in the account's growing queue will be assigned a lower priority to avoid clogging the queue with a single account's queue.
5.  **Account Class of Service** - Accounts can be assigned classes of service to indicate priority treatment. A high-priority account that has 20 running jobs may get a higher priority than a low-priority account that has 10 running jobs.
6.  **User assigned priority** - <span>Priority can be set per flavor in a specific transcoding profile to indicate the importance of flavors (for example, when the mobile app has more views than your website, publishers can configure the iPhone and iPad flavors to have a higher priority than the web flavors). I</span><span>t is also possible to configure different priorities between an accounts transcoding profiles, to enable the content uploader to choose the priority of their media entry. Transcoding priority </span><span>can be set via API when manually queuing conversion jobs.</span>

<h3 id="KalturaMediaTranscodingServicesandTechnology-OtherPriorityControlsandTranscodingManagementTools">
  Other Priority Controls and Transcoding Management Tools
</h3>

1.  **Job Quota** - A quota can be configured to limit the number of concurrently running jobs in the Kaltura deployment. There is a system-wide default as well as defaults for specific job types. It is also possible to configure the quota differently per each account.
2.  **Express Queue** - There are several batch workers that are limited to small transcoding jobs (i.e. configured to transcode short duration videos exclusively). This ensures a short wait time for shorter videos, even when many long videos are ingested to the system. 
3.  **Dedicated (Reserved) Transcoders** - It is possible to configure workers that process only jobs of certain publisher accounts. This allows publishers to reserve dedicated transcoders for their jobs (for example, 8 dedicated transcoders guarantees immediate processing for 8 transcoding jobs at any given time, and any additional jobs will be handled by the shared transcoding queue). This ensures that time-sensitive publishing workflows always have reserved resources in deployments where system resources may be constrained. 
4.  **Priority Boost** - Kaltura platform operators, can boost the priority of specific transcoding jobs from within the Admin Console, to manually increase the priority of a waiting job.
5.  **Moving Jobs** - Transcoding jobs can be balanced between Kaltura Data Centers. As such, if one DC has a longer-than-usual queue of transcoding jobs, it is possible to move jobs to another Kaltura DC after the source video file was synchronized to the other DC.
6.  <span><strong>Remote Transcoding</strong> - Kaltura's batch framework and distributed API-based architecture allows for running transcoding jobs remotely as an extension of the Kaltura deployment. For example, a load on a private local Kaltura deployment gets higher than usual priority, Kaltura operators can provision machines on a public cloud (such as IBM Bluemix, Amazon Web Services, Google Cloud, or Rackspace) and easily configure these remote Kaltura batch workers to pull the source files form the local Kaltura deployment, perform the transcoding job, and push the transcoded assets back to the local deployment. Batch workers use the Kaltura API (and never access the data base directly), as such remote transcoding is easy to setup, secure and automate, and there is no requirement to setup VPN tunnels or mess with complex network security configurations.</span>

<p class="wiki-content">
  <a href="#top">Back to top.</a>
</p>

<h2 id="KalturaMediaTranscodingServicesandTechnology-TranscodingTimesandQualityofService">
  <a name="qos"></a>Transcoding Times and Quality of Service
</h2>

For applications and workflows where fast turnaround is essential, such as sports, breaking news, surveillance, Ad Tech, and social media, fast video queueing time and processing times are highly important to satisfy user expectations and support critical operations. 

To ensure best quality and smallest file size optimization the transcoding time of a given source file depends highly on the type of content in the video; For example, a highly dynamic scene, with changing lighting and high level of detail (e.g. nature walk) will achieve different results than a static scene (e.g. talking head) or a scene with low level of details (e.g. text slides). On a single transcoding worker (without segmented parallel transcoding) typical transcoding times are as follows:

*   For 360p video, transcoding will usually be realtime (i.e. equal to the duration of the source video). 
*   For 720p video, transcoding will usually be between 4x and 8x the video duration. 
*   For 1080p video, transcoding will usually be between 10x to 15x of the video duration. 

Beyond transcoding time and quality, the following considerations are built into Kaltura's architecture to ensure optimal quality of service and SLA.

*   **Queuing Time**: For 90% of all videos uploaded to Kaltura SaaS, video transcoding begins within 3 seconds after upload complete. For 10% of videos, transcoding generally begins within 3 seconds to 3 minutes. 
*   **Playback Availability**: With Kaltura, all video is transcoded in parallel, utilizing as many system resources and workers available to the Kaltura deployment. Video is generally available as soon as the first flavor is available and for high-priority immediate / live requirements Kaltura utilizes dedicated transcoders, and priority settings.
*   **Scale**: With Kaltura, publishers can define unlimited number of transcoding profiles, and execute unlimited number of transcoding jobs.
*   **Control**: With Kaltura, publishers can set a wide variety of configurations to customize and optimize the transcoding workflows for their business needs and requirements.

Video file encryption (i.e. data-at-rest or Widevine) is encrypted at a much higher rate than video transcoding, and generally is faster than real-time. 

[Back to top.][14]

<h2 id="KalturaMediaTranscodingServicesandTechnology-ProgrammaticMediaAuthoringAPIandTools">
  <a name="tools"></a>Programmatic Media Authoring API and Tools
</h2>

<span>Format and codec transcoding is merely where your journey with video begins. To support the many video experiences and workflows required for video operations, Kaltura Media Transcoding Services feature a wide range of authoring and editing tools, ranging from </span><span>thumbnail generation through Image watermarks and overlays, sub-clip creation and trimming. Use the UI tools for quick tweaking of your videos, or the Kaltura APIs to build creative video manipulations at scale.</span>

<span>The following lists a few of the common video authoring scenarios achievable with the Kaltura Media Transcoding Services:</span>

<h3 id="KalturaMediaTranscodingServicesandTechnology-Real-timeThumbnailsCreation">
  <span>Real-time Thumbnails Creation</span>
</h3>

<a href="http://knowledge.kaltura.com/node/228" target="_blank" class="external-link" rel="nofollow">The Kaltura Thumbnail API</a> provides a simple web interface to dynamically generate image snapshots of Kaltura video entries on the fly. Generated images are generated upon demand, and caching is managed on disk and CDN levels. The result of the thumbnail API is a JPEG, PNG or GIF image, and provides many image manipulation tools, including;

*   Image re-sizing and frame cropping.
*   Extracting specific frame from a video clip on.
*   Thumbnail versions caching.
*   <span>Various compression quality controls.</span>
*   <span>Generation of JPG sprites for optimal delivery and use as CSS sprites.</span>
*   <span>Applying overlays and templates.</span>

<h3 id="KalturaMediaTranscodingServicesandTechnology-Watermarking" class="p1">
  <span class="s1">Watermarking</span>
</h3>

<p class="p1">
  <span class="s1">When defining a new video flavor, publishers can include an image overlay for watermarking setting using PNG or JPG image formats as the watermark. The watermark image will be burnt on the video flavor at the specified coordinates and dimensions (relatively to video frame borders). Scaling, opacity and transparency are also supported. The watermark image can be another Kaltura entry of type image, or a URL pointing to the watermark image.</span>
</p>

<h3 id="KalturaMediaTranscodingServicesandTechnology-Sub-ClippingandTrimming" class="p3">
  <span class="s1">Sub-Clipping and Trimming</span>
</h3>

<p class="p4">
  <span class="s1">Publishers can leverage the clipping and trimming tool to define an offset and duration, that in turn either creates a new clip of the source video, or trims the beginning and end of the video.</span>
</p>

<h3 id="KalturaMediaTranscodingServicesandTechnology-AudioEnhancements" class="p3">
  <span class="s1">Audio Enhancements</span>
</h3>

<ul class="ul1">
  <li class="li1">
    <span class="s1"><strong>Multiple audio streams</strong> - Upon detection of a source containing multiple-audio streams, the transcoding logic attempts to match it with known audio layouts (e.g. <a href="http://en.wikipedia.org/wiki/5.1_surround_sound" class="external-link" rel="nofollow">5.1</a>, <a href="http://en.wikipedia.org/wiki/7.1_surround_sound" class="external-link" rel="nofollow">7.1</a>). If such a match is detected, the following can be performed: </span><ul class="ul1">
      <li class="li1">
        <span class="s1">The multi-channel audio can be down-mixed to stereo. </span>
      </li>
      <li class="li1">
        <span class="s1">The first channel can be chosen as the audio source. </span>
      </li>
      <li class="li1">
        <span class="s1">The flavor can be customized to force a specific audio channels mapping.</span>
      </li>
    </ul>
  </li>
  
  <li class="li1">
    <span class="s1"><strong>Noise reduction and normalizing volume level</strong> - through custom settings on the flavor level, noise reduction filters as well as volume level settings can be applied to the transcoded assets.</span>
  </li>
</ul>

<h3 id="KalturaMediaTranscodingServicesandTechnology-FrameRotation" class="li1">
  <span class="s1">Frame Rotation</span>
</h3>

<span class="s1">Rotation is often an important setting with videos recorded on mobile device.  To ensure correct orientation of uploaded video, Kaltura automatically detects camera rotation and rotates the video frame accordingly to ensure mobile captured videos are always viewable on the correct rotation. </span>

<h3 id="KalturaMediaTranscodingServicesandTechnology-AdvancedVideoCoding">
  Advanced Video Coding 
</h3>

Depending on the chosen video transcoding engine, Kaltura exposes a wide range of capabilities including controlling the gopsize, frame rate, bitrate, 2-pass as well as automatic filters such as <a href="http://en.wikipedia.org/wiki/Deinterlacing" target="_blank" class="external-link" rel="nofollow">deinterlicing</a> and more.

[Back to top.][14]

<h2 id="KalturaMediaTranscodingServicesandTechnology-BatchArchitectureandBackendPlugins" class="li1">
  <span class="s1"><a name="plugins"></a>Batch Architecture and Backend Plugins</span>
</h2>

<p class="p2">
  <span class="s1">The Kaltura Media Transcoding Services are implemented as a Kaltura batch workers. See <a href="http://knowledge.kaltura.com/node/230" target="_blank" class="external-link" rel="nofollow">Introduction to Kaltura Batch Processes</a> to learn more about batch processes and the Kaltura batch architecture.</span>
</p>

<p class="p2">
  <span class="s1">To ensure ease of extensibility and allow for adding new transcoding engines and capabilities, the Kaltura Media Transcoding Services are built on the <a href="http://knowledge.kaltura.com/node/430" target="_blank" class="external-link" rel="nofollow">Kaltura Backend Plugins Framework</a>. Transcoding server plugins are configured and </span><span class="s2">registered automatically with the Kaltura batch managers, who activate the plugin worker for all job types that are assigned to that backend plugin.</span>
</p>

<p class="p3">
  <span class="s1">When activated, the plugin implementation extends the specific encoding engine API (often command line interface, or web interface) to perform, manage and monitor the required transcoding tasks it needs to carry. Transcoding server plugins run engines that vary from command line binary tools (for example ffmpeg) to API based encoder integrations (for example using Harmonic Encoders' proprietary API). Upon completion of the transcoding job, the plugin informs the batch manager of completion, any error states and the output asset files.</span>
</p>

<p class="p3">
  <span class="s1"><a href="#top">Back to top.</a></span>
</p>

<h2 class="p3">
  <span class="s1"><a name="dedicated"></a>Dedicated Transcoding</span>
</h2>

**What is Dedicated Transcoding?**

Under normal circumstances, when an asset is uploaded into Kaltura, the video the client uploads is put into a first-in-first-out transcode queue with other (non-dedicated) Kaltura customers (note: batch actions are given lower priority). Dedicated transcoding aims to ensure the video the client uploads is transcoded immediately, and not queued.

**Terminology**

1.  Job – the work of transcoding a single source video file to a single flavor.
2.  Worker – a process that executes a single job at a time, for example, a machine that has 10 workers will have at most 10 running jobs in parallel.

**What is a VCore?**

*   A “core” is a single Central Processing Unit (CPU), basically the part of the server that does the main processing of the software logic.
*   A virtual machine (VM) is where the functions of a single machine (or server) are simulated instead of being directly tied to a single physical server.
*   Putting both of these concepts together (VM and Core) helps understand what a VCore (or virtual core) is.
*   You can have a single physical server with six physical cores. You could then have three VMs running on this one physical server, where each VM has two VCores. Each VM “thinks and acts” like it is a single physical machine with two cores.

<p class="page view">
  <span class="mce-note-graphic">Since ffmpeg can work with several threads, on a 20 core server it is not recommended to run 20 ffmpeg's, it may be better to run, for example, only 10. If we use 20 workers, then yes 20 videos are guaranteed to start processing immediately, but they will run slower than if we use only 10 workers.</span>
</p>

**How many videos can be transcoded at the same time?**

*   The number of videos (x) that can be transcoded simultaneously is directly proportional to the number of VCores (y).
*   The client is therefore only guaranteed that x videos will transcode with zero wait time if they also have y VCores (i.e. where x=y).
*   If the client uploads more than x videos at once, and only has y VCores (where y < x), then some videos go into the normal Kaltura transcode queue with all other client’s videos.

**Can some videos from a single KMC use the dedicated transcoders and others not?**

*   Often not all content within a single KMC needs to be treated with the same priority.
*   Certain urgent content (such as news or gossip content) can be transcoded immediately via the dedicated transcoders.
*   The standard, less urgent content can then go through the normal queue.

**How does dedicated transcoding work?**

*   The single transcode of an asset is known as a job.
*   A job (and therefore transcode) can be assigned a priority.
*   Kaltura can assign a set number of VCores to only work on jobs that have a given priority (and KMC ID).
*   Individual transcode profiles can be associated with individual priorities. Kaltura can also go down to the flavor level if needed. For example, the iPad flavor will use dedicated transcoding and the iPhone flavor will not.
*   Since uploaded videos are assigned transcode profiles, by extension therefore, uploaded videos can be assigned to specific jobs (i.e. certain VCores).
*   If you want to have some videos trafficked through the dedicated transcoders (such as news) and other less urgent videos added to the normal queue, you need a different transcode profile to be assigned to the specific video.
*   The end result: if you set a given transcode profile to a newly created entry, the entry will be prioritised accordingly.

**What are the steps to implement dedicated transcoding?**

<span class="mce-note-graphic">Assigning the priorities to flavors / conversion profiles can only be done by Kaltura at this point (can't be done via API)</span>

1.  Create a transcode profile to be used for urgent videos, i.e. news content.
2.  Create a transcode profile to be used for non-urgent videos, i.e. normal content.
3.  Programmatically, insert the appropriate transcode profile ID into the dropfolder XML based on the type of content.
4.  The content is sent to either a queued job or dedicated job, depending on the associated transcode profile ID.

**What information does Kaltura require from the client?**

1.  <span>At which data centER do they want the VCores applied</span>? The options are: just the west coast, just the east coast or split between the two (for example, if the customer bought 30 CPUs, we can have 20 in the EC and 10 in the WC. This decision should be based on the DC the client most often gets data from, and the geo location of the most uploads.
2.  KMC ID
3.  Number of VCores  
    *   As described, the number of videos (x) that can be transcoded simultaneously is directly proportional to the number of VCores (y).
    *   For there to be no wait time, x must equal y.
    *   For example, if the client wants to be able to transcode 10 videos at the same time they w2ill need 10 VCores.
4.  Transcode Profile ID (only relevant if segregating content into queued vs dedicated for a single KMC).

<p class="p3">
  <span class="s1">For additional information about dedicated transcoding, please contact your Kaltura Account Manager.</span>
</p>

<p class="p3">
  <span class="s1"><a href="#top">Back to top.</a></span>
</p>