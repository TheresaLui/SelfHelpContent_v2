<properties
	pageTitle="Issue creating a search service"
	description="Issue creating a search service"
	service="microsoft.search"
	resource="searchservices"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="resource"
	displayOrder="80"
	supportTopicIds="32681355"
	resourceTags=""
	productPesIds="15568"
	articleId="create-search-service"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating a search service

## **Recommended Steps**

### **General issues creating a search service**  

If you are having trouble creating an Azure Cognitive Search service, you should ensure that:

1.	You have access to create resources within your Azure subscription
2.	You have provided a unique name for your search service and followed the naming guidelines found [here](https://docs.microsoft.com/azure/search/search-create-service-portal)
3.	You have selected a [supported region](https://azure.microsoft.com/pricing/details/search/) for Azure Cognitive Search
4.	You have allowed adequate time for the Azure Cognitive Search service to be deployed. This typically occurs within minutes and can be monitored through Azure notifications.  In some cases, services on the Basic tier may take up to 90 minutes to provision.  This should be relatively rare, but please allow this much time to pass before opening a support case.
5.	You have not already used your allotted number of free search services.  By default, each subscription is allowed only one free search service.

## **Recommended Documents**

* [Quickstart: Create an Azure Cognitive Search service in the portal](https://docs.microsoft.com/azure/search/search-create-service-portal)
* [Azure Search service quick start template](https://github.com/Azure/azure-quickstart-templates/tree/master/101-azure-search-create)
