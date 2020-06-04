<properties
	pageTitle="Issue adding or removing partitions or replicas"
	description="Issue adding or removing partitions or replicas"
	service="microsoft.search"
	resource="searchservices"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="resource"
	displayOrder="23"	
	supportTopicIds="32681352"
	resourceTags=""
	productPesIds="15568"
	articleId="partitions-and-replicas"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue adding or removing partitions or replicas

## **Recommended Steps**

If you are having troubles adding or removing partitions and replicas in your Azure Cognitive Search service, you may want to ensure that you:

1.	Are using the Azure portal for the scaling operation, which enforces limits on allowable [combinations](https://docs.microsoft.com/azure/search/search-capacity-planning) of replicas & partitions that stay below maximum service limits
2.	Have not exceeded the [storage limits](https://docs.microsoft.com/azure/search/search-limits-quotas-capacity) of the current Search service tier (SKU). You can easily review this during the scale operation as the formula at the bottom of the Scale page indicates how many search units are being utilized.
3.	Have allowed adequate time for the scaling operation to complete.  Changes in capacity take several hours to complete and cannot be cancelled one the process has started.  

## **Recommended Documents**

* [Scale up partitions and replicas to add capacity for query index workloads in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-capacity-planning)
