<properties
	pageTitle="Portal/I can’t scale the service in the portal"
	description="Issues scaling an Azure Cognitive Search service in the portal"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="3"
	supportTopicIds="32681347"
	resourceTags=""
	productPesIds="15568"
	articleId="portal-cant-scale-service"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issues with Azure Cognitive Search portal search explorer

## **Recommended Steps**

If you are having issues scaling an Azure Cognitive Search service in the portal, here are the most common reasons:

* Timeframe:  It is important to note that adding and removing search units to a search service does not complete immediately.  It is not uncommon to take an hour to fully scale up a search service.  This can be further impacted if there is large amounts of data in the search service.
* Tier Migration: It is not currently possible to migrate an Azure Search service from one tier (SKU) to another.  If you require a service to be created in a different tier, you will need to create a new search service and re-create the indexes.  In some cases, the [following tool](https://docs.microsoft.com/samples/azure-samples/azure-search-dotnet-samples/azure-search-backup-restore-index/) can help with the data copy, but it is important to make note of the caveats in this page.
* Controls are disabled:  This most likely indicates your search service is in a provisioning state (perhaps from a previous scaling attempt) and you should wait for this to complete and periodically refresh the portal.  If this lasts for multiple hours, please contact customer support.


## **Recommended Documents**

* [Backup/Restore Index Tool](https://docs.microsoft.com/samples/azure-samples/azure-search-dotnet-samples/azure-search-backup-restore-index/)