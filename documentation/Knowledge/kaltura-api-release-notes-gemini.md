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

 

<span>added enum value </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. ESTIMATED_EFFORT_ASC</span>  
<span>added enum value </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. ESTIMATED_EFFORT_DESC</span>  
<span>added enum value </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. LOCK_EXPIRATION_ASC</span>  
<span>added enum value </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobOrderBy" target="_blank">KalturaBatchJobOrderBy</a><span>. LOCK_EXPIRATION_DESC</span>  
<span>added parameter </span><a href="https://developer.kaltura.com/api-docs/#/flavorAsset.convert" target="_blank">flavorAsset.convert</a><span>.priority</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.createdAtGreaterThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.createdAtLessThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.estimatedEffortGreaterThan</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.estimatedEffortLessThan</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.executionAttemptsGreaterThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.executionAttemptsLessThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.idEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.idGreaterThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockExpirationGreaterThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockExpirationLessThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockVersionGreaterThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.lockVersionLessThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.partnerIdEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.partnerIdIn</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.partnerIdNotIn</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.updatedAtGreaterThanOrEqual</span>  
<span>added property </span><a href="https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter" target="_blank">KalturaBatchJobBaseFilter</a><span>.updatedAtLessThanOrEqual</span>  
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
<span class="mce-heading-3">Drop Folder Improvements</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaDropFolderErrorCode" target="_blank">KalturaDropFolderErrorCode</a>  
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
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaDropFolderContentProcessorJobData" target="_blank">KalturaDropFolderContentProcessorJobData</a>  
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
<span class="mce-heading-3">Widevine DRM</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorAssetOrderBy" target="_blank">KalturaWidevineFlavorAssetOrdeeBy</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsOrderBy" target="_blank">KalturaWidevineFlavorParamsOrderBy</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsOutputOrderBy" target="_blank">KalturaWidevineFlavorParamsOutputOrderBy</a>  
<span>added enum value </span>[KalturaAssetType][13]<span>.WIDEVINE_FLAVOR</span>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorAsset" target="_blank">KalturaWidevineFlavorAsset</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorAssetBaseFilter" target="_blank">KalturaWidevineFlavorAssetBaseFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorAssetFilter" target="_blank">KalturaWidevineFlavorAssetFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParams" target="_blank">KalturaWidevineFlavorParams</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsBaseFilter" target="_blank">KalturaWidevineFlavorParamsBaseFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsFilter" target="_blank">KalturaWidevineFlavorParamsFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsOutput" target="_blank">KalturaWidevineFlavorParamsOutput</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsOutputBaseFilter" target="_blank">KalturaWidevineFlavorParamsOutputBaseFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaWidevineFlavorParamsOutputFilter" target="_blank">KalturaWidevineFlavorParamsOutputFilter</a>  
<span>added plugin widevine</span>  
<span>added property </span>[KalturaEntryContextDataParams][14]<span>.flavorTags</span>  
<span>added property </span>[KalturaEntryContextDataResult][15]<span>.flavorAssets</span>  
<span>added service </span>[widevineDrm][16]  
<span class="mce-heading-3">Access Control Enhancements</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaLimitFlavorsRestrictionType" target="_blank">KalturaLimitFlavorsRestrictionType</a>  
<span>added enum value </span>[KalturaAccessControlActionType][17]<span>.LIMIT_FLAVORS</span>  
<span>added enum value </span>[KalturaAccessControlContextType][18]<span>.METADATA</span>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAccessControlLimitFlavorsAction" target="_blank">KalturaAccessControlLimitFlavorsAction</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaLimitFlavorsRestriction" target="_blank">KalturaLimitFlavorsRestriction</a>  
<span>added property </span>[KalturaAccessControlScope][19]<span>.hashes</span>  
<span class="mce-heading-3">Universal Live Stream and DVR</span><span>added action </span>[liveStream.isLive][20]  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAkamaiUniversalStreamType" target="_blank">KalturaAkamaiUniversalStreamType</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaDVRStatus" target="_blank">KalturaDVRStatus</a>  
<span>added enum value </span>[KalturaSourceType][21]<span>.AKAMAI_UNIVERSAL_LIVE</span>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAkamaiUniversalProvisionJobData" target="_blank">KalturaAkamaiUniversalProvisionJobData</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaLiveStreamConfiguration" target="_blank">KalturaLiveStreamConfiguration</a>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.dvrStatus</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.dvrWindow</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.hlsStreamUrl</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.liveStreamConfigurations</span>  
<span>added property </span>[KalturaLiveStreamEntry][22]<span>.urlManager</span>  
<span class="mce-heading-3">Embed Code Enhancements</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaPlaybackProtocol" target="_blank">KalturaPlaybackProtocol</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaPlayerDeliveryType" target="_blank">KalturaPlayerDeliveryType</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaPlayerEmbedCodeType" target="_blank">KalturaPlayerEmbedCodeType</a>  
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
<span class="mce-heading-3">Event Notifications</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationFormat" target="_blank">KalturaEmailNotificationFormat</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationRecipientProviderType" target="_blank">KalturaEmailNotificationRecipientProviderType</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventNotificationEventObjectType" target="_blank">KalturaEventNotificationEventObjectType</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventNotificationEventType" target="_blank">KalturaEventNotificationEventType</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationCategoryRecipientJobData" target="_blank">KalturaEmailNotificationCategoryRecipientJobData</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationCategoryRecipientProvider" target="_blank">KalturaEmailNotificationCategoryRecipientProvider</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationRecipient" target="_blank">KalturaEmailNotificationRecipient</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationRecipientJobData" target="_blank">KalturaEmailNotificationRecipientJobData</a>  
<span>added object </span>[KalturaEmailNotificationRecipientProvider][28]  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationStaticRecipientJobData" target="_blank">KalturaEmailNotificationStaticRecipientJobData</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationStaticRecipientProvider" target="_blank">KalturaEmailNotificationStaticRecipientProvider</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationTemplate" target="_blank">KalturaEmailNotificationTemplate</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationUserRecipientJobData" target="_blank">KalturaEmailNotificationUserRecipientJobData</a>  
<span>added object </span>[KalturaEmailNotificationUserRecipientProvider][29]  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventCondition" target="_blank">KalturaEventCondition</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventFieldCondition" target="_blank">KalturaEventFieldCondition</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventNotificationParameter" target="_blank">KalturaEventNotificationParameter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventNotificationTemplate" target="_blank">KalturaEventNotificationTemplate</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEventNotificationTemplateListResponse" target="_blank">KalturaEventNotificationTemplateListResponse</a>  
<span>added plugin eventNotification</span>  
<span>added service </span>[eventNotificationTemplate][30]  
<span class="mce-heading-3">MRSS Feed Improvements</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaCategoryIdentifierField" target="_blank">KalturaCategoryIdentifierField</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEntryIdentifierField" target="_blank">KalturaEntryIdentifierField</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaMrssExtensionMode" target="_blank">KalturaMrssExtensionMode</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaCategoryIdentifier" target="_blank">KalturaCategoryIdentifier</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEntryIdentifier" target="_blank">KalturaEntryIdentifier</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExtendingItemMrssParameter" target="_blank">KalturaExtendingItemMrssParameter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaObjectIdField" target="_blank">KalturaObjectIdField</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaObjectIdentifier" target="_blank">KalturaObjectIdentifier</a>  
<span>added parameter </span>[media.getMrss][31]<span>.extendingItemsArray</span>  
<span class="mce-heading-3">External Entry Support</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExternalMediaEntryOrderBy" target="_blank">KalturaExternalMediaEntryOrderBy</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExternalMediaSourceType" target="_blank">KalturaExternalMediaSourceType</a>  
<span>added enum value </span>[KalturaEntryType][32]<span>.EXTERNAL_MEDIA</span>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExternalMediaEntry" target="_blank">KalturaExternalMediaEntry</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExternalMediaEntryBaseFilter" target="_blank">KalturaExternalMediaEntryBaseFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExternalMediaEntryFilter" target="_blank">KalturaExternalMediaEntryFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaExternalMediaEntryListResponse" target="_blank">KalturaExternalMediaEntryListResponse</a>  
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
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaCategoryUserProviderFilter" target="_blank">KalturaCategoryUserProviderFilter</a>  
<span>added property </span>[KalturaCategoryUser][44]<span>.permissionNames</span>  
<span>added property </span>[KalturaCategoryUserBaseFilter][45]<span>.permissionNamesMatchAnd</span>  
<span>added property </span>[KalturaCategoryUserBaseFilter][45]<span>.permissionNamesMatchOr</span>  
<span>added property </span>[KalturaCategoryUserBaseFilter][45]<span>.permissionNamesNotContains</span>  
<span>added property </span>[KalturaUserFilter][40]<span>.permissionNamesMultiLikeAnd</span>  
<span>added property </span>[KalturaUserFilter][40]<span>.permissionNamesMultiLikeOr</span>  
<span class="mce-heading-3">Generic Asset Distribution</span>  
<span>added enum value </span>[KalturaConditionType][46]<span>.ASSET_PROPERTIES_COMPARE</span>  
<span>added enum value </span>[KalturaDistributionErrorType][47]<span>.MISSING_ASSET</span>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAssetDistributionCondition" target="_blank">KalturaAssetDistributionCondition</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAssetDistributionPropertyCondition" target="_blank">KalturaAssetDistributionPropertyCondition</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAssetDistributionRule" target="_blank">KalturaAssetDistributionRule</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAssetPropertiesCompareCondition" target="_blank">KalturaAssetPropertiesCompareCondition</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaDistributionValidationErrorMissingAsset" target="_blank">KalturaDistributionValidationErrorMissingAsset</a>  
<span>added property </span>[KalturaDistributionProfile][48]<span>.optionalAssetDistributionRules</span>  
<span>added property </span>[KalturaDistributionProfile][48]<span>.requiredAssetDistributionRules</span>  
<span>added property </span>[KalturaEntryDistribution][49]<span>.assetIds</span>  
<span class="mce-heading-3">Analytics</span><span>added enum value </span>[KalturaReportType][50]<span>.BROWSERS</span>  
<span>added enum value </span>[KalturaReportType][50]<span>.OPERATION_SYSTEM</span>  
<span>added enum value </span>[KalturaReportType][50]<span>.PLATFORMS</span>  
<span>added enum value </span>[KalturaReportType][50]<span>.TOP_CREATORS</span>  
<span>added property </span>[KalturaReportInputBaseFilter][51]<span>.fromDay</span>  
<span>added property </span>[KalturaReportInputBaseFilter][51]<span>.toDay</span>  
<span class="mce-heading-3">Amazon S3 Remote Storage</span><span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAmazonS3StorageProfileFilesPermissionLevel" target="_blank">KalturaAmazonS3StorageProfileFilesPermissionLevel</a>  
<span>added enum </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAmazonS3StorageProfileOrderBy" target="_blank">KalturaAmazonS3StorageProfileOrderBy</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAmazonS3StorageExportJobData" target="_blank">KalturaAmazonS3StorageExportJobData</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAmazonS3StorageProfile" target="_blank">KalturaAmazonS3StorageProfile</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAmazonS3StorageProfileBaseFilter" target="_blank">KalturaAmazonS3StorageProfileBaseFilter</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaAmazonS3StorageProfileFilter" target="_blank">KalturaAmazonS3StorageProfileFilter</a>  
<span class="mce-heading-3">Related Entries</span><span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaContext" target="_blank">KalturaContext</a>  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaEntryContext" target="_blank">KalturaEntryContext</a>  
<span>added parameter </span>[][52][playlist.execute][53]<span>.filter</span>  
<span>added parameter </span>[playlist.execute][54]<span>.playlistContext</span>  
<span class="mce-heading-3">Annotation Fields</span><span>added property </span>[KalturaAnnotation][55]<span>.childrenCount</span>  
<span>added property </span>[KalturaAnnotation][55]<span>.depth</span>  
<span>added property </span>[KalturaAnnotation][55]<span>.directChildrenCount</span>  
<span class="mce-heading-3">Hosted Pages Support</span><span>added action </span>[][52][session.get][56]  
<span>added action </span>[session.impersonateByKs][57]  
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaSessionInfo" target="_blank">KalturaSessionInfo</a>  
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
<span>added object </span><a href="https://developer.kaltura.com/api-docs/#/KalturaDeleteFileJobData" target="_blank">KalturaDeleteFileJobData</a>  
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

 [1]: https://developer.kaltura.com/api-docs/#/KalturaBatchJobOrderBy
 [2]: https://developer.kaltura.com/api-docs/#/KalturaBatchJobBaseFilter
 [3]: https://developer.kaltura.com/api-docs/#/KalturaBatchJobType
 [4]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderFileErrorCode
 [5]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderFileStatus
 [6]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderStatus
 [7]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderType
 [8]: https://developer.kaltura.com/api-docs/#/KalturaDropFolder
 [9]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderBaseFilter
 [10]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderFile
 [11]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderFileBaseFilter
 [12]: https://developer.kaltura.com/api-docs/#/KalturaDropFolderFilter
 [13]: https://developer.kaltura.com/api-docs/#/KalturaAssetType
 [14]: https://developer.kaltura.com/api-docs/#/KalturaEntryContextDataParams
 [15]: https://developer.kaltura.com/api-docs/#/KalturaEntryContextDataResult
 [16]: https://developer.kaltura.com/api-docs/#/widevineDrm
 [17]: https://developer.kaltura.com/api-docs/#/KalturaAccessControlActionType
 [18]: https://developer.kaltura.com/api-docs/#/KalturaAccessControlContextType
 [19]: https://developer.kaltura.com/api-docs/#/KalturaAccessControlScope
 [20]: https://developer.kaltura.com/api-docs/#/liveStream.isLive
 [21]: https://developer.kaltura.com/api-docs/#/KalturaSourceType
 [22]: https://developer.kaltura.com/api-docs/#/KalturaLiveStreamEntry
 [23]: https://developer.kaltura.com/api-docs/#/KalturaPartner
 [24]: https://developer.kaltura.com/api-docs/#/KalturaAudioCodec
 [25]: https://developer.kaltura.com/api-docs/#/KalturaContainerFormat
 [26]: https://developer.kaltura.com/api-docs/#/KalturaVideoCodec
 [27]: https://developer.kaltura.com/api-docs/#/KalturaFlavorParams
 [28]: https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationRecipientProvider
 [29]: https://developer.kaltura.com/api-docs/#/KalturaEmailNotificationUserRecipientProvider
 [30]: https://developer.kaltura.com/api-docs/#/eventNotificationTemplate
 [31]: https://developer.kaltura.com/api-docs/#/media.getMrss
 [32]: https://developer.kaltura.com/api-docs/#/KalturaEntryType
 [33]: https://developer.kaltura.com/api-docs/#/externalMedia
 [34]: https://developer.kaltura.com/api-docs/#/document.approveReplace
 [35]: https://developer.kaltura.com/api-docs/#/document.cancelReplace
 [36]: https://developer.kaltura.com/api-docs/#/document.updateContent
 [37]: https://developer.kaltura.com/api-docs/#/documents.approveReplace
 [38]: https://developer.kaltura.com/api-docs/#/documents.cancelReplace
 [39]: https://developer.kaltura.com/api-docs/#/documents.updateContent
 [40]: https://developer.kaltura.com/api-docs/#/KalturaUserFilter
 [41]: https://developer.kaltura.com/api-docs/#/KalturaUserRole
 [42]: https://developer.kaltura.com/api-docs/#/KalturaUserRoleBaseFilter
 [43]: https://developer.kaltura.com/api-docs/#/KalturaCategoryUserPermissionLevel
 [44]: https://developer.kaltura.com/api-docs/#/KalturaCategoryUser
 [45]: https://developer.kaltura.com/api-docs/#/KalturaCategoryUserBaseFilter
 [46]: https://developer.kaltura.com/api-docs/#/KalturaConditionType
 [47]: https://developer.kaltura.com/api-docs/#/KalturaDistributionErrorType
 [48]: https://developer.kaltura.com/api-docs/#/KalturaDistributionProfile
 [49]: https://developer.kaltura.com/api-docs/#/KalturaEntryDistribution
 [50]: https://developer.kaltura.com/api-docs/#/KalturaReportType
 [51]: https://developer.kaltura.com/api-docs/#/KalturaReportInputBaseFilter
 [52]: http://www.kaltura.com/api_v3/testmeDoc/?service=%3Ca%20href=
 [53]: https://developer.kaltura.com/api-docs/#/playlist.execute
 [54]: https://developer.kaltura.com/api-docs/#/playlist.execute
 [55]: https://developer.kaltura.com/api-docs/#/KalturaAnnotation
 [56]: https://developer.kaltura.com/api-docs/#/session.get
 [57]: https://developer.kaltura.com/api-docs/#/session.impersonateByKs
 [58]: https://developer.kaltura.com/api-docs/#/KalturaDistributionProtocol
 [59]: https://developer.kaltura.com/api-docs/#/aspera
 [60]: https://developer.kaltura.com/api-docs/#/metadata.updateFromXSL
 [61]: https://developer.kaltura.com/api-docs/#/system.getTime
 [62]: https://developer.kaltura.com/api-docs/#/tag.deletePending
 [63]: https://developer.kaltura.com/api-docs/#/user.index
 [64]: https://developer.kaltura.com/api-docs/#/KalturaCaptionType
 [65]: https://developer.kaltura.com/api-docs/#/KalturaFeatureStatusType
 [66]: https://developer.kaltura.com/api-docs/#/KalturaUiConfObjType
 [67]: https://developer.kaltura.com/api-docs/#/partner.register
 [68]: https://developer.kaltura.com/api-docs/#/thumbAsset.getUrl
 [69]: https://developer.kaltura.com/api-docs/#/thumbAsset.serve
 [70]: https://developer.kaltura.com/api-docs/#/KalturaBulkUploadCsvJobData
 [71]: https://developer.kaltura.com/api-docs/#/KalturaImportJobData
 [72]: https://developer.kaltura.com/api-docs/#/KalturaStorageProfile
 [73]: https://developer.kaltura.com/api-docs/#/KalturaVarPartnerUsageItem
 [74]: https://developer.kaltura.com/api-docs/#/KalturaWidget
