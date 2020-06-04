<properties
	pageTitle="Issue moving a search service between subscriptions"
	description="Issue moving a search service between subscriptions"
	service="microsoft.search"
	resource="searchservices"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="resource"
	displayOrder="22"	
	supportTopicIds="32681370"
	resourceTags=""
	productPesIds="15568"
	articleId="moving-search-service"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue moving a search service between subscriptions

It is important to note that both the source group and the target group are locked during the move operation.  Write and delete operations are blocked on the resource groups until the move completes and you will not be able to add, update or delete resources in the resource groups during this time, but does not mean that the resources are frozen.

## **Recommended Steps**

If you want to move your Azure Cognitive Search service to a new subscription you will want to ensure that:

1. You have reviewed the [Checklist](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources) before moving resources
2. Both the source and destination subscriptions are active
3. Both the source and destination subscriptions must exist with the same [Azure Active Directory tenant](https://docs.microsoft.com/azure/active-directory/develop/quickstart-create-new-tenant)
4. The account moving the resources has the following permissions:

	* **Microsoft.Resources/subscriptions/resourceGroups/moveResources/action** on the source resource group
	* **Microsoft.Resources/subscriptions/resourceGroups/write** on the destination resource group
	
5. If moving between subscriptions, ensure that the Azure Cognitive Search resource and all its dependent resources are located in the same Resource Group and are being moved together
6. Use the [validate move](https://docs.microsoft.com/rest/api/resources/resources/validatemoveresources) operation to test your move scenario without actually moving the resources.  This operation will check if the move will succeed.

## **Recommended Documents**

* [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Scenario for move across subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#scenario-for-move-across-subscriptions)
* [Resources – Validate move resources](https://docs.microsoft.com/rest/api/resources/resources/validatemoveresources)
