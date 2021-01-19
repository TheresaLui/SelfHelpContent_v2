<properties
	pageTitle="Who accessed my storage resource"
	description="Who accessed my storage resource"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="Lea"
	ms.author="leakkari"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32748846,32749537,32749538,32749539,32749540"
	resourceTags=""
	productPesIds="15629,16459,16460,16598,16462,16461"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="9fa460ce-5ada-43f8-ae2d-5aaf3d477f4c"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Who accessed my storage resource

## **Recommended Steps**

Storage Analytics logs detailed information about successful requests and failed requests to a storage service. You can use this information to monitor individual requests and to diagnose issues with a storage service.

Storage Analytics is not enabled by default for your storage account. You can enable it in the Azure portal, or programmatically, through the REST API or the client library. You can also use the Get Blob Service Properties, Get Queue Service Properties, and Get Table Service Properties operations to enable Storage Analytics for each service.

For more information, see [Storage Analytics](https://docs.microsoft.com/azure/storage/common/storage-analytics?toc=/azure/storage/blobs/toc.jsonhttps://docs.microsoft.com/rest/api/storageservices/storage-analytics-log-format#log-entry-format-20).

After it's enabled, you can use [Storage Analytics Log 2.0 to check logging information about requests authorized with an OAuth 2.0 token provided by Azure Active Directory(Azure AD)](https://docs.microsoft.com/rest/api/storageservices/storage-analytics-log-format#log-entry-format-20)

**Note**:
On August 31, 2023. Storage Analytics metrics, also referred to as "classic metrics," will be retired. For more information, see the [official announcement](https://azure.microsoft.com/updates/azure-storage-classic-metrics-will-be-retired-on-31-august-2023/). If you use classic metrics, make sure to transition to metrics in Azure Monitor prior to that date. This article will help you make the transition.
