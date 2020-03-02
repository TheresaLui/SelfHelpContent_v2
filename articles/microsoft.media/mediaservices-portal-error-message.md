<properties
	pageTitle="Azure Media Services Portal error messages"
	description="Azure Media Services Portal error messages"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-portal-error-message"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632091"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Services Portal error messages

**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

## **Recommended Steps**

**Disconnected Media or Storage Account Error**

The "Disconnected" state for a Media Services account indicates that the account no longer has access to one or more of the attached storage accounts due to a change in storage access keys. Up-to-date storage access keys are required by Media Services to perform many tasks in the account.

The following are the primary scenarios that would result in a Media Services account not having access to attached storage accounts. Please review and fix if any of these apply:

1.  The Media Services account or attached storage account(s) were migrated to separate subscriptions. Migrate the storage account(s) or Media Services account so that they are all in the same subscription. 
2.  The Media Services account is using an attached storage account in a different subscription as it was an early Media Services account where this was supported. All early Media Services accounts were converted to modern Azure Resources Manager (ARM) based accounts and will have a Disconnected state. Migrate the storage account or Media Services account so that they are all in the same subscription.

## **Recommended Documents**

* [Get Started with Azure AD Authentication in the portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-get-started-with-aad)<br>
* [Get started with delivering content on demand by using the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-vod-get-started)<br>
* [How to perform live streaming with on-premises encoders using the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-live-passthrough-get-started)<br>
* [Manage streaming endpoints with the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-manage-streaming-endpoints)<br>
* [Upload files to a Media Services account in the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-upload-files)<br>
* [Encode an asset by using Media Encoder Standard in the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-encode)<br>
* [Scale your media processing reserved units in the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-scale-media-processing)<br>
* [Scale streaming endpoints with the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-scale-streaming-endpoints)<br>
* [Monitor encoding job progress in the Azure portal](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-check-job-progress)<br>
* [Create and monitor Media Services events with Event Grid using the Azure portal](https://docs.microsoft.com/azure/media-services/latest/monitor-events-portal-how-to)

