<properties
    pageTitle="Need to scale Media Reserved Units"
    description="Need to scale Media Reserved Units"
    infoBubbleText=""
	service="microsoft.media"
	resource="mediaservices"
    authors="ReutAmior"
    ms.author="t-reutam"
    displayOrder="1"
    articleId="mediaservices-videoindexer-manage-ru"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32740746,32740748"
    resourceTags=""
    productPesIds="16535"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_Media_VI"
/>

# Need to scale Media Reserved Units

Videos may take a long time to index if they are waiting in the Reserved Units queue.

A Media Services account is associated with a Reserved Unit Type, which determines the speed with which your media processing tasks are processed. You can pick between the following reserved unit types: S1, S2, or S3. In addition to specifying the reserved unit type, you can specify to provision your account with Reserved Units (RUs). The number of provisioned RUs determines the number of media tasks that can be processed concurrently in each account.

**For indexing purposes, we recommend adjusting the type and number of Reserved Units to at least 10 S3 Reserved Units in your Media Services account.**

### Auto-scaling Reserved Units in Video Indexer

Video Indexer offers an option to automatically scale reserved units. This way, you can allocate the maximum number of RUs and be sure that Video Indexer stops/starts RUs automatically. With this option, you don't pay extra money for idle time but also do not wait for indexing jobs to complete a long time when the indexing load is high.

## **Recommended Steps**

### Use the auto-scale option in Video Indexer

If auto-scaling is not turned on in your account:

1.	Go to the **Settings** page in the Video Indexer portal
2.	Change the auto-scale option to **On** to allow more Reserved Unit when they are needed

### Create a service request to increase the Reserved Units quota

If you have already reached the default limit of Reserved Units (10 S3 units), create a service request to increase it. Learn how to open a support ticket in the link below.

## **Recommended Documents**

* [How to create a service request to increase RUs quota](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors#solution)
* [Auto-scale reserved units in Video Indexer](https://docs.microsoft.com/azure/media-services/video-indexer/manage-account-connected-to-azure#auto-scale-reserved-units)
* [Scaling Media Processing overview](https://docs.microsoft.com/azure/media-services/previous/media-services-scale-media-processing-overview)
* [Change the reserved unit type](https://docs.microsoft.com/azure/media-services/previous/media-services-portal-scale-media-processing)
* [Scale media processing with CLI](https://docs.microsoft.com/azure/media-services/latest/media-reserved-units-cli-how-to)
