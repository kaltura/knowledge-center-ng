---
layout: page
title: "Kaltura API Release Notes for Gemini"
date: 2013-04-25 11:45:20
---

**Version: Gemini 7.1.4**

**Revision: 97242**

These release notes pertain to the Kaltura API changes for Gemini, released April, 2013. These release notes are intended for developers who want to use Kaltura's Application Programming Interfaces (APIs).

<h4 class="mce-heading-2">
  What's New in this Release?
</h4>

<p class="mce-heading-3">
  Batch Job Enhancments
</p>

 

<span>added enum value </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. ESTIMATED_EFFORT_ASC</span>  
<span>added enum value </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. ESTIMATED_EFFORT_DESC</span>  
<span>added enum value </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. LOCK_EXPIRATION_ASC</span>  
<span>added enum value </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. LOCK_EXPIRATION_DESC</span>  
<span>added parameter </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?service=flavorAsset&action=convert" target="_blank">flavorAsset.convert</a><span>.priority</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.createdAtGreaterThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.createdAtLessThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.estimatedEffortGreaterThan</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.estimatedEffortLessThan</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.executionAttemptsGreaterThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.executionAttemptsLessThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.idEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.idGreaterThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockExpirationGreaterThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockExpirationLessThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockVersionGreaterThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockVersionLessThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.partnerIdEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.partnerIdIn</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.partnerIdNotIn</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.updatedAtGreaterThanOrEqual</span>  
<span>added property </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.updatedAtLessThanOrEqual</span>  
<span>removed enum value FILE_SIZE_ASC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value FILE_SIZE_DESC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value PROCESSOR_EXPIRATION_ASC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value PROCESSOR_EXPIRATION_DESC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value PROGRESS_ASC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value PROGRESS_DESC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value UPDATES_COUNT_ASC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed enum value UPDATES_COUNT_DESC from </span>[KalturaBatchJobOrderBy][1]  
<span>removed property fileSizeGreaterThan from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property fileSizeLessThan from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property lastWorkerRemoteEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property onStressDivertToEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property onStressDivertToIn from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property onStressDivertToNotIn from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property progressGreaterThanOrEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property progressLessThanOrEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property twinJobIdEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property twinJobIdIn from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property twinJobIdNotIn from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property updatesCountGreaterThanOrEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span>removed property updatesCountLessThanOrEqual from </span>[KalturaBatchJobBaseFilter][2]  
<span class="mce-heading-3">Drop Folder Improvements</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderErrorCode" target="_blank">KalturaDropFolderErrorCode</a>  
<span>added enum value </span>[KalturaBatchJobType][3]<span>.DROP_FOLDER_CONTENT_PROCESSOR</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.ERROR_ADDING_CONTENT_PROCESSOR</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.ERROR_ADD_CONTENT_RESOURCE</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.ERROR_DELETING_FILE</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.ERROR_IN_BULK_UPLOAD</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.ERROR_IN_CONTENT_PROCESSOR</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.ERROR_UPDATE_FILE</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.FILE_NO_MATCH</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.MALFORMED_XML_FILE</span>  
<span>added enum value </span>[KalturaDropFolderFileErrorCode][4]<span>.XML_FILE_SIZE_EXCEED_LIMIT</span>  
<span>added enum value </span>[KalturaDropFolderFileStatus][5]<span>.DETECTED</span>  
<span>added enum value </span>[KalturaDropFolderFileStatus][5]<span>.PARSED</span>  
<span>added enum value </span>[KalturaDropFolderFileStatus][5]<span>.PROCESSING</span>  
<span>added enum value </span>[KalturaDropFolderStatus][6]<span>.ERROR</span>  
<span>added enum value </span>[KalturaDropFolderType][7]<span>.S3</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderContentProcessorJobData" target="_blank">KalturaDropFolderContentProcessorJobData</a>  
<span>added property </span>[KalturaDropFolder][8]<span>.errorCode</span>  
<span>added property </span>[KalturaDropFolder][8]<span>.errorDescription</span>  
<span>added property </span>[KalturaDropFolder][8]<span>.lastAccessedAt</span>  
<span>added property </span>[KalturaDropFolderBaseFilter][9]<span>.errorCodeEqual</span>  
<span>added property </span>[KalturaDropFolderBaseFilter][9]<span>.errorCodeIn</span>  
<span>added property </span>[KalturaDropFolderBaseFilter][9]<span>.pathEqual</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.batchJobId</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.deletedDropFolderFileId</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.entryId</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.importEndedAt</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.importStartedAt</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.leadDropFolderFileId</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.uploadEndDetectedAt</span>  
<span>added property </span>[KalturaDropFolderFile][10]<span>.uploadStartDetectedAt</span>  
<span>added property </span>[KalturaDropFolderFileBaseFilter][11]<span>.deletedDropFolderFileIdEqual</span>  
<span>added property </span>[KalturaDropFolderFileBaseFilter][11]<span>.entryIdEqual</span>  
<span>added property </span>[KalturaDropFolderFileBaseFilter][11]<span>.leadDropFolderFileIdEqual</span>  
<span>added property </span>[KalturaDropFolderFilter][12]<span>.currentDc</span>  
<span>removed enum value DROP_FOLDER_HANDLER from </span>[KalturaBatchJobType][3]  
<span class="mce-heading-3">Widevine DRM</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorAssetOrderBy" target="_blank">KalturaWidevineFlavorAssetOrdeeBy</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsOrderBy" target="_blank">KalturaWidevineFlavorParamsOrderBy</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsOutputOrderBy" target="_blank">KalturaWidevineFlavorParamsOutputOrderBy</a>  
<span>added enum value </span>[KalturaAssetType][13]<span>.WIDEVINE_FLAVOR</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorAsset" target="_blank">KalturaWidevineFlavorAsset</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorAssetBaseFilter" target="_blank">KalturaWidevineFlavorAssetBaseFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorAssetFilter" target="_blank">KalturaWidevineFlavorAssetFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParams" target="_blank">KalturaWidevineFlavorParams</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsBaseFilter" target="_blank">KalturaWidevineFlavorParamsBaseFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsFilter" target="_blank">KalturaWidevineFlavorParamsFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsOutput" target="_blank">KalturaWidevineFlavorParamsOutput</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsOutputBaseFilter" target="_blank">KalturaWidevineFlavorParamsOutputBaseFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidevineFlavorParamsOutputFilter" target="_blank">KalturaWidevineFlavorParamsOutputFilter</a>  
<span>added plugin widevine</span>  
<span>added property </span>[KalturaEntryContextDataParams][14]<span>.flavorTags</span>  
<span>added property </span>[KalturaEntryContextDataResult][15]<span>.flavorAssets</span>  
<span>added service </span>[widevineDrm][16]  
<span class="mce-heading-3">Access Control Enhancements</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaLimitFlavorsRestrictionType" target="_blank">KalturaLimitFlavorsRestrictionType</a>  
<span>added enum value </span>[KalturaAccessControlActionType][17]<span>.LIMIT_FLAVORS</span>  
<span>added enum value </span>[KalturaAccessControlContextType][18]<span>.METADATA</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAccessControlLimitFlavorsAction" target="_blank">KalturaAccessControlLimitFlavorsAction</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaLimitFlavorsRestriction" target="_blank">KalturaLimitFlavorsRestriction</a>  
<span>added property </span>[KalturaAccessControlScope][19]<span>.hashes</span>  
<span class="mce-heading-3">Universal Live Stream and DVR</span><span>added action </span>[liveStream.isLive][20]  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAkamaiUniversalStreamType" target="_blank">KalturaAkamaiUniversalStreamType</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDVRStatus" target="_blank">KalturaDVRStatus</a>  
<span>added enum value </span>[KalturaSourceType][21]<span>.AKAMAI_UNIVERSAL_LIVE</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAkamaiUniversalProvisionJobData" target="_blank">KalturaAkamaiUniversalProvisionJobData</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaLiveStreamConfiguration" target="_blank">KalturaLiveStreamConfiguration</a>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.dvrStatus</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.dvrWindow</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.hlsStreamUrl</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.liveStreamConfigurations</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.urlManager</span>  
<span class="mce-heading-3">Embed Code Enhancements</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaPlaybackProtocol" target="_blank">KalturaPlaybackProtocol</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaPlayerDeliveryType" target="_blank">KalturaPlayerDeliveryType</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaPlayerEmbedCodeType" target="_blank">KalturaPlayerEmbedCodeType</a>  
<span>added property </span>[KalturaPartner][23]<span>.defaultDeliveryType</span>  
<span>added property </span>[KalturaPartner][23]<span>.defaultEmbedCodeType</span>  
<span>added property </span>[KalturaPartner][23]<span>.deliveryTypes</span>  
<span>added property </span>[KalturaPartner][23]<span>.embedCodeTypes</span>  
<span class="mce-heading-3">Transcoding</span><span>added enum value </span>[KalturaAudioCodec][24]<span>.AACHE</span>  
<span>added enum value </span>[KalturaAudioCodec][24]<span>.PCM</span>  
<span>added enum value </span>[KalturaContainerFormat][25]<span>.COPY</span>  
<span>added enum value </span>[KalturaContainerFormat][25]<span>.OGV</span>  
<span>added enum value </span>[KalturaContainerFormat][25]<span>.WAV</span>  
<span>added enum value </span>[KalturaContainerFormat][25]<span>.WVM</span>  
<span>added enum value </span>[KalturaVideoCodec][26]<span>.APCH</span>  
<span>added enum value </span>[KalturaVideoCodec][26]<span>.APCN</span>  
<span>added enum value </span>[KalturaVideoCodec][26]<span>.APCO</span>  
<span>added enum value </span>[KalturaVideoCodec][26]<span>.APCS</span>  
<span>added enum value </span>[KalturaVideoCodec][26]<span>.DNXHD</span>  
<span>added enum value </span>[KalturaVideoCodec][26]<span>.DV</span>  
<span>added property </span>[KalturaFlavorParams][27]<span>.anamorphicPixels</span>  
<span>added property </span>[KalturaFlavorParams][27]<span>.isAvoidForcedKeyFrames</span>  
<span>added property </span>[KalturaFlavorParams][27]<span>.isAvoidVideoShrinkBitrateToSource</span>  
<span>added property </span>[KalturaFlavorParams][27]<span>.isAvoidVideoShrinkFramesizeToSource</span>  
<span>added property </span>[KalturaFlavorParams][27]<span>.isVideoFrameRateForLowBrAppleHls</span>  
<span>added property </span>[KalturaFlavorParams][27]<span>.maxFrameRate</span>  
<span class="mce-heading-3">Event Notifications</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationFormat" target="_blank">KalturaEmailNotificationFormat</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationRecipientProviderType" target="_blank">KalturaEmailNotificationRecipientProviderType</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventNotificationEventObjectType" target="_blank">KalturaEventNotificationEventObjectType</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventNotificationEventType" target="_blank">KalturaEventNotificationEventType</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationCategoryRecipientJobData" target="_blank">KalturaEmailNotificationCategoryRecipientJobData</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationCategoryRecipientProvider" target="_blank">KalturaEmailNotificationCategoryRecipientProvider</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationRecipient" target="_blank">KalturaEmailNotificationRecipient</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationRecipientJobData" target="_blank">KalturaEmailNotificationRecipientJobData</a>  
<span>added object </span>[KalturaEmailNotificationRecipientProvider][28]  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationStaticRecipientJobData" target="_blank">KalturaEmailNotificationStaticRecipientJobData</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationStaticRecipientProvider" target="_blank">KalturaEmailNotificationStaticRecipientProvider</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationTemplate" target="_blank">KalturaEmailNotificationTemplate</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationUserRecipientJobData" target="_blank">KalturaEmailNotificationUserRecipientJobData</a>  
<span>added object </span>[KalturaEmailNotificationUserRecipientProvider][29]  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventCondition" target="_blank">KalturaEventCondition</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventFieldCondition" target="_blank">KalturaEventFieldCondition</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventNotificationParameter" target="_blank">KalturaEventNotificationParameter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventNotificationTemplate" target="_blank">KalturaEventNotificationTemplate</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEventNotificationTemplateListResponse" target="_blank">KalturaEventNotificationTemplateListResponse</a>  
<span>added plugin eventNotification</span>  
<span>added service </span>[eventNotificationTemplate][30]  
<span class="mce-heading-3">MRSS Feed Improvements</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCategoryIdentifierField" target="_blank">KalturaCategoryIdentifierField</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryIdentifierField" target="_blank">KalturaEntryIdentifierField</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaMrssExtensionMode" target="_blank">KalturaMrssExtensionMode</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCategoryIdentifier" target="_blank">KalturaCategoryIdentifier</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryIdentifier" target="_blank">KalturaEntryIdentifier</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExtendingItemMrssParameter" target="_blank">KalturaExtendingItemMrssParameter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaObjectIdField" target="_blank">KalturaObjectIdField</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaObjectIdentifier" target="_blank">KalturaObjectIdentifier</a>  
<span>added parameter </span>[media.getMrss][31]<span>.extendingItemsArray</span>  
<span class="mce-heading-3">External Entry Support</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExternalMediaEntryOrderBy" target="_blank">KalturaExternalMediaEntryOrderBy</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExternalMediaSourceType" target="_blank">KalturaExternalMediaSourceType</a>  
<span>added enum value </span>[KalturaEntryType][32]<span>.EXTERNAL_MEDIA</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExternalMediaEntry" target="_blank">KalturaExternalMediaEntry</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExternalMediaEntryBaseFilter" target="_blank">KalturaExternalMediaEntryBaseFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExternalMediaEntryFilter" target="_blank">KalturaExternalMediaEntryFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaExternalMediaEntryListResponse" target="_blank">KalturaExternalMediaEntryListResponse</a>  
<span>added plugin externalMedia</span>  
<span>added service </span>[externalMedia][33]  
<span class="mce-heading-3">Document Replacement Flow</span><span>added action </span>[document.approveReplace][34]  
<span>added action </span>[document.cancelReplace][35]  
<span>added action </span>[document.updateContent][36]  
<span>added action </span>[documents.approveReplace][37]  
<span>added action </span>[documents.cancelReplace][38]  
<span>added action </span>[documents.updateContent][39]  
<span class="mce-heading-3">Roles and  Permissions Filters</span><span>added property </span>[KalturaUserFilter][40]<span>.roleIdsEqual</span>  
<span>added property </span>[KalturaUserFilter][40]<span>.roleIdsIn</span>  
<span>added property </span>[KalturaUserRole][41]<span>.systemName</span>  
<span>added property </span>[KalturaUserRoleBaseFilter][42]<span>.systemNameEqual</span>  
<span>added property </span>[KalturaUserRoleBaseFilter][42]<span>.systemNameIn</span>  
<span class="mce-heading-3">CategoryUser Permissions</span><span>added enum value </span>[KalturaCategoryUserPermissionLevel][43]<span>.NONE</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCategoryUserProviderFilter" target="_blank">KalturaCategoryUserProviderFilter</a>  
<span>added property </span>[KalturaCategoryUser][44]<span>.permissionNames</span>  
<span>added property </span>[KalturaCategoryUserBaseFilter][45]<span>.permissionNamesMatchAnd</span>  
<span>added property </span>[KalturaCategoryUserBaseFilter][45]<span>.permissionNamesMatchOr</span>  
<span>added property </span>[KalturaCategoryUserBaseFilter][45]<span>.permissionNamesNotContains</span>  
<span>added property </span>[KalturaUserFilter][40]<span>.permissionNamesMultiLikeAnd</span>  
<span>added property </span>[KalturaUserFilter][40]<span>.permissionNamesMultiLikeOr</span>  
<span class="mce-heading-3">Generic Asset Distribution</span>  
<span>added enum value </span>[KalturaConditionType][46]<span>.ASSET_PROPERTIES_COMPARE</span>  
<span>added enum value </span>[KalturaDistributionErrorType][47]<span>.MISSING_ASSET</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAssetDistributionCondition" target="_blank">KalturaAssetDistributionCondition</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAssetDistributionPropertyCondition" target="_blank">KalturaAssetDistributionPropertyCondition</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAssetDistributionRule" target="_blank">KalturaAssetDistributionRule</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAssetPropertiesCompareCondition" target="_blank">KalturaAssetPropertiesCompareCondition</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDistributionValidationErrorMissingAsset" target="_blank">KalturaDistributionValidationErrorMissingAsset</a>  
<span>added property </span>[KalturaDistributionProfile][48]<span>.optionalAssetDistributionRules</span>  
<span>added property </span>[KalturaDistributionProfile][48]<span>.requiredAssetDistributionRules</span>  
<span>added property </span>[KalturaEntryDistribution][49]<span>.assetIds</span>  
<span class="mce-heading-3">Analytics</span><span>added enum value </span>[KalturaReportType][50]<span>.BROWSERS</span>  
<span>added enum value </span>[KalturaReportType][50]<span>.OPERATION_SYSTEM</span>  
<span>added enum value </span>[KalturaReportType][50]<span>.PLATFORMS</span>  
<span>added enum value </span>[KalturaReportType][50]<span>.TOP_CREATORS</span>  
<span>added property </span>[KalturaReportInputBaseFilter][51]<span>.fromDay</span>  
<span>added property </span>[KalturaReportInputBaseFilter][51]<span>.toDay</span>  
<span class="mce-heading-3">Amazon S3 Remote Storage</span><span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAmazonS3StorageProfileFilesPermissionLevel" target="_blank">KalturaAmazonS3StorageProfileFilesPermissionLevel</a>  
<span>added enum </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAmazonS3StorageProfileOrderBy" target="_blank">KalturaAmazonS3StorageProfileOrderBy</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAmazonS3StorageExportJobData" target="_blank">KalturaAmazonS3StorageExportJobData</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAmazonS3StorageProfile" target="_blank">KalturaAmazonS3StorageProfile</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAmazonS3StorageProfileBaseFilter" target="_blank">KalturaAmazonS3StorageProfileBaseFilter</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAmazonS3StorageProfileFilter" target="_blank">KalturaAmazonS3StorageProfileFilter</a>  
<span class="mce-heading-3">Related Entries</span><span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaContext" target="_blank">KalturaContext</a>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryContext" target="_blank">KalturaEntryContext</a>  
<span>added parameter </span>[][52][playlist.execute][53]<span>.filter</span>  
<span>added parameter </span>[playlist.execute][54]<span>.playlistContext</span>  
<span class="mce-heading-3">Annotation Fields</span><span>added property </span>[KalturaAnnotation][55]<span>.childrenCount</span>  
<span>added property </span>[KalturaAnnotation][55]<span>.depth</span>  
<span>added property </span>[KalturaAnnotation][55]<span>.directChildrenCount</span>  
<span class="mce-heading-3">Hosted Pages Support</span><span>added action </span>[][52][session.get][56]  
<span>added action </span>[session.impersonateByKs][57]  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaSessionInfo" target="_blank">KalturaSessionInfo</a>  
<span class="mce-heading-3">Aspera Plugin</span><span>added enum value </span>[KalturaDistributionProtocol][58]<span>.ASPERA</span>  
<span>added plugin aspera</span>  
<span>added service </span>[aspera][59]  
<span class="mce-heading-3">Misc</span><span>added action </span>[metadata.updateFromXSL][60]  
<span>added action </span>[system.getTime][61]  
<span>added action </span>[tag.deletePending][62]  
<span>added action </span>[user.index][63]  
<span>added enum value </span>[KalturaBatchJobType][3]<span>.TAG_RESOLVE</span>  
<span>added enum value </span>[KalturaCaptionType][64]<span>.WEBVTT</span>  
<span>added enum value </span>[KalturaFeatureStatusType][65]<span>.USER</span>  
<span>added enum value </span>[KalturaUiConfObjType][66]<span>.KSR</span>  
<span>added enum value </span>[KalturaUiConfObjType][66]<span>.KUPLOAD</span>  
<span>added object </span><a href="http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDeleteFileJobData" target="_blank">KalturaDeleteFileJobData</a>  
<span>added parameter </span>[partner.register][67]<span>.silent</span>  
<span>added parameter </span>[thumbAsset.getUrl][68]<span>.thumbParams</span>  
<span>added parameter </span>[thumbAsset.serve][69]<span>.thumbParams</span>  
<span>added property </span>[KalturaBulkUploadCsvJobData][70]<span>.columns</span>  
<span>added property </span>[KalturaImportJobData][71]<span>.fileSize</span>  
<span>added property </span>[KalturaPartner][23]<span>.cdnHost</span>  
<span>added property </span>[KalturaPartner][23]<span>.host</span>  
<span>added property </span>[KalturaPartner][23]<span>.ignoreSeoLinks</span>  
<span>added property </span>[KalturaPartner][23]<span>.isFirstLogin</span>  
<span>added property </span>[KalturaPartner][23]<span>.language</span>  
<span>added property </span>[KalturaPartner][23]<span>.logoutUrl</span>  
<span>added property </span>[KalturaPartner][23]<span>.rtmpUrl</span>  
<span>added property </span>[KalturaPartner][23]<span>.templatePartnerId</span>  
<span>added property </span>[KalturaStorageProfile][72]<span>.allowAutoDelete</span>  
<span>added property </span>[KalturaVarPartnerUsageItem][73]<span>.deletedStorage</span>  
<span>added property </span>[KalturaWidget][74]<span>.addEmbedHtml5Support</span>

 [1]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobOrderBy
 [2]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobBaseFilter
 [3]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBatchJobType
 [4]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderFileErrorCode
 [5]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderFileStatus
 [6]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderStatus
 [7]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderType
 [8]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolder
 [9]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderBaseFilter
 [10]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderFile
 [11]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderFileBaseFilter
 [12]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDropFolderFilter
 [13]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAssetType
 [14]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryContextDataParams
 [15]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryContextDataResult
 [16]: http://www.kaltura.com/api_v3/testmeDoc/?service=widevine_widevinedrm
 [17]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAccessControlActionType
 [18]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAccessControlContextType
 [19]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAccessControlScope
 [20]: http://www.kaltura.com/api_v3/testmeDoc/?service=liveStream&action=isLive
 [21]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaSourceType
 [22]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaLiveStreamEntry
 [23]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaPartner
 [24]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAudioCodec
 [25]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaContainerFormat
 [26]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaVideoCodec
 [27]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaFlavorParams
 [28]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationRecipientProvider
 [29]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEmailNotificationUserRecipientProvider
 [30]: http://www.kaltura.com/api_v3/testmeDoc/?service=eventnotification_eventnotificationtemplate
 [31]: http://www.kaltura.com/api_v3/testmeDoc/?service=media&action=getMrss
 [32]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryType
 [33]: http://www.kaltura.com/api_v3/testmeDoc/?service=externalmedia_externalmedia
 [34]: http://www.kaltura.com/api_v3/testmeDoc/?service=document&action=approveReplace
 [35]: http://www.kaltura.com/api_v3/testmeDoc/?service=document&action=cancelReplace
 [36]: http://www.kaltura.com/api_v3/testmeDoc/?service=document&action=updateContent
 [37]: http://www.kaltura.com/api_v3/testmeDoc/?service=documents&action=approveReplace
 [38]: http://www.kaltura.com/api_v3/testmeDoc/?service=documents&action=cancelReplace
 [39]: http://www.kaltura.com/api_v3/testmeDoc/?service=documents&action=updateContent
 [40]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaUserFilter
 [41]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaUserRole
 [42]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaUserRoleBaseFilter
 [43]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCategoryUserPermissionLevel
 [44]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCategoryUser
 [45]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCategoryUserBaseFilter
 [46]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaConditionType
 [47]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDistributionErrorType
 [48]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDistributionProfile
 [49]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaEntryDistribution
 [50]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaReportType
 [51]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaReportInputBaseFilter
 [52]: http://www.kaltura.com/api_v3/testmeDoc/?service=%3Ca%20href=
 [53]: http://www.kaltura%3C/a%3E.com/api_v3/testmeDoc/?service=playlist&action=execute
 [54]: http://www.kaltura.com/api_v3/testmeDoc/?service=playlist&action=execute
 [55]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaAnnotation
 [56]: http://www.kaltura%3C/a%3E.com/api_v3/testmeDoc/?service=session&action=get
 [57]: http://www.kaltura.com/api_v3/testmeDoc/?service=session&action=impersonateByKs
 [58]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaDistributionProtocol
 [59]: http://www.kaltura.com/api_v3/testmeDoc/?service=aspera_aspera
 [60]: http://www.kaltura.com/api_v3/testmeDoc/?service=metadata&action=updateFromXSL
 [61]: http://www.kaltura.com/api_v3/testmeDoc/?service=system&action=getTime
 [62]: http://www.kaltura.com/api_v3/testmeDoc/?service=tag&action=deletePending
 [63]: http://www.kaltura.com/api_v3/testmeDoc/?service=user&action=index
 [64]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaCaptionType
 [65]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaFeatureStatusType
 [66]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaUiConfObjType
 [67]: http://www.kaltura.com/api_v3/testmeDoc/?service=partner&action=register
 [68]: http://www.kaltura.com/api_v3/testmeDoc/?service=thumbAsset&action=getUrl
 [69]: http://www.kaltura.com/api_v3/testmeDoc/?service=thumbAsset&action=serve
 [70]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaBulkUploadCsvJobData
 [71]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaImportJobData
 [72]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaStorageProfile
 [73]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaVarPartnerUsageItem
 [74]: http://www.kaltura.com/api_v3/testmeDoc/?object=KalturaWidget