<properties
	pageTitle="Issue deleting a search service"
	description="Issue deleting a search service"
	service="microsoft.search"
	resource="searchservices"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="resource"
	displayOrder="5"	
	supportTopicIds="32681361"
	resourceTags=""
	productPesIds="15568"
	articleId="delete-search-service"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue deleting a search service

Deleting a service deletes everything on it. There is no facility within Azure Cognitive Search for backing up and restoring persisted search data. Please be sure you are deleting the correct Azure Cognitive Search service before proceeding.

## **Recommended Steps**

If you are having trouble deleting your Azure Cognitive Search service, you may want to ensure that:

1.	You have typed in the Azure Cognitive Search service name exactly as it appears in the Azure Portal
2.	You have permissions to delete resources from your Azure subscription
3.	You have allowed adequate time for the Azure Cognitive Search service to be deleted. This can be monitored through Azure notifications.

## **Recommended Documents**

* To delete your Search service programmatically, refer to [this](https://docs.microsoft.com/rest/api/searchmanagement/Services/Delete) document
