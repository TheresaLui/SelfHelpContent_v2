<properties
	pageTitle="Azure Media Services linking and managing storage accounts"
	description="Azure Media Services linking and managing storage accounts"
	infoBubbleText=""
	service="microsoft.media"
	resource="mediaservices"
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-accounts-linking-storage-accts"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632104"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Services linking and managing storage accounts

Azure Media Services supports multiple storage accounts. You can link an existing storage account, or create a new storage account prior to the creation of your Media Services account and pass it in to the create call. 

The Media Services account and all associated storage accounts must be in the same Azure subscription. It is strongly recommended to use storage accounts in the same location as the Media Services account to avoid additional latency and data egress costs.


## **Recommended Steps**


* Follow the instructions on how to create a new Media Services account with a new storage account - [Create an Azure Media Services account with storage accounts](https://docs.microsoft.com/azure/media-services/latest/create-account-cli-how-to#create-a-storage-account)

### Add a storage account to your Media Services account using the CLI

1. Open the Cloud Shell or CLI locally and run the following command to see the options:
   
```
	az ams account storage -h
```

2. To attach a "secondary" storage account, use the following CLI command to see the options:
   
```
	az ams account storage add -h
```

3. To remove a "secondary" storage account, use the following CLI command to see the options:
   
```
	az ams account storage remove -h
```

### Troubleshoot access issues with linked storage accounts

It is possible for keys to be rotated on a storage account and get out of sync with the Media Services account. To forces a resync of the storage keys, run the following CLI command to see the options.

```
	az ams account storage sync-storage-keys -h
```

## **Recommended Documents**

* [Azure Media Services v3 overview](https://docs.microsoft.com/azure/media-services/latest/media-services-overview)
* [Cloud upload and storage](https://docs.microsoft.com/azure/media-services/latest/storage-account-concept)
* [Create an Azure Media Services account with storage accounts](https://docs.microsoft.com/azure/media-services/latest/create-account-cli-how-to#create-a-storage-account)

