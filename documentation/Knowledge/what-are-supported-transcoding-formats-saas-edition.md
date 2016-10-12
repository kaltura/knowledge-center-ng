---
layout: page
title: "What are the supported Transcoding formats for the SaaS edition?"
date: 2011-12-21 14:37:28
---

<h3 id="KalturaMediaTranscodingServicesandTechnology-CommonlyUsedVideoFormatsandCodecs">
  <strong>Commonly Used Video Formats and Codecs </strong>
</h3>

The following lists commonly used media formats and codecs that were tested and optimized for transcoding and delivery by Kaltura.

<p class="mce-note-graphic">
  Additional codecs and formats are supported by the underlying encoder engines and can be ingested and transcoded by Kaltura. For further details and discovery regarding a specific codec or format that is not listed, please <a href="http://corp.kaltura.com/company/contact-us" class="external-link" rel="nofollow">contact us</a>.
</p>

<h4 id="KalturaMediaTranscodingServicesandTechnology-Ingest(Input)FileFormatsandCodecs">
  Ingest (Input) File Formats and Codecs
</h4>

The following video formats and codecs have been tested and optimized for optimal transcoding input:

**Media File Formats: **Mpeg-4 and QuickTime Formats (MP4, MOV, QT, and M4V), Flash Video (FLV and F4V), Microsoft Windows Formats (AVI, ASF, WMV and WMA), MPEG-1/2 (MPG, M1V, M2V, MP3), WAV, Matroska (MKV), OGG OGM & OGV, WEBM, 3GP, RM, Webex (ARF), MXF

**Video Codecs: **DivX (Div3/4/5, DX50), DV, H.263, H.264 and AVC, MPEG-4 Visual, MPEG-1/2, MJPG, MP42/3, IV40/50 (Indeo codecs), RV30/40, RMVB, FLV1/4, VP3/5/6/7/8/9, Sorenson (SVQ1/3), Xvid, Theora, WMV1/2/3, VC1, ProRes 422, ICOD, DVCPRO, PXLT, TCSS/TCS2, GoToMeeting Codec (G2M3/4)

<p class="mce-note-graphic">
  The Maximum Video Frame Size is 5000 x 5000.
</p>

**Audio Codecs: **MP3, MP1/2, AC3, AAC, Vorbis, AMR, PCM, WMA7/8/9, WMSpeech, FLAC, QDM2, RA, Nellymoser, Cook, GSM, SPEEX 

<h4 id="KalturaMediaTranscodingServicesandTechnology-Target(Output)VideoandAudioCodecs">
  Target (Output) Video and Audio Codecs 
</h4>

The following video formats and codecs have been tested and optimized as optimal transcoding output and delivery:

****Media File** Formats: **MP4, FLV, AVI, 3GP, OGG, MKV, WMV, WMA, Microsoft Silverlight Smooth Streaming, Apple HTTP Live Streaming (HLS), WEBM, MPEG, MPEG TS, WAV, M4V, MXF

**Video Codecs: **H.265, H.264, H.263, MPEG-4 Visual, VP9, VP8, VP6, FLV1, Theora, WMV1/2, VC1, MPEG-2, APCN/S/O/H, DNXHD, DV

**Audio Codecs: **MP3, AAC LC, AAC HE, Vorbis, WMA/Pro, AMR NB, MPEG2, AC3, PCM

<h3 id="KalturaMediaTranscodingServicesandTechnology-Delivery-specificFormats">
  Delivery-specific Formats
</h3>

Kaltura supports various streaming standards and protocols, see the <a href="http://knowledge.kaltura.com/node/880" class="external-link" rel="nofollow">Video Delivery Settings article</a> for more information about the types of video delivery formats support and supported delivery settings in Kaltura.

<h3 id="KalturaMediaTranscodingServicesandTechnology-intermediateIntermediate-SourceProcessing">
  Intermediate-Source Processing
</h3>

With some proprietary formats and codecs, a dedicated hardware, operating system or software may be required to handle the transcoding of such files. In such cases Kaltura will leverage the dedicated technology to convert the ingested proprietary source into an intermediate-source (file of non-proprietary format/codec, usually MP4/H.264 or WMV) and then continue the processing as usual.

For example, read: <a href="http://knowledge.kaltura.com/node/723" class="external-link" rel="nofollow">Best Practices For Uploading Content Created Using Screencast Tools</a>.

*   Webex/ARF - <a href="http://www.webex.com/play-webex-recording.html" class="external-link" rel="nofollow">Cisco's WebEx Network Recording Tool</a> will be used to covert the proprietary WebEx format before continuing with the media transcoding process.
*   GoToMeeting Codec - Windows Expression Encoder 4 will be used to covert the proprietary GoToMeeting codec before continuing with the media transcoding process.
*   QuickTime Video (QT) - MAC machines will be used to covert the proprietary QT format before continuing with the media transcoding process.

In addition to processing 'special source formats', an intermediate-source is also used to handle known video issues, such as handling artifacts in Digital Video sources, adding silent audio tracks for assets that will be ciphered by Widevine DRM, and other cases.