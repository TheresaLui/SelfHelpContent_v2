<properties
	pageTitle="Configure the new storage account"
	description="Configure the new storage account"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b2dbd392-7bca-4e12-866f-d8cd39b33b77"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Configure the new storage account 

Some features won't export to a template, so you'll have to add them to the new storage account. The following table lists these features along with guidance for adding them to your new storage account.  

1. Lifecycle management policies : [Manage the Azure Blob storage lifecycle](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal) 
2. Static websites: [Host a static website in Azure Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website-how-to?tabs=azure-portal) 
3. Event subscriptions: [Reacting to Blob storage events](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-event-overview) 
4. Alerts: [Create, view, and manage activity log alerts by using Azure Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/alerts-activity-log) 
5. Content Delivery Network (CDN): [Use Azure CDN to access blobs with custom domains over HTTPS](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-https-custom-domain-cdn) 

Note: If you set up a CDN for the source storage account, just change the origin of your existing CDN to the primary blob service endpoint (or the primary static website endpoint) of your new account.
