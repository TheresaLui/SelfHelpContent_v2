<properties
	pageTitle="Performance|Low memory query failures" <!-- metadata only  -->
	description="Performance|Low memory query failures" <!-- metadata only -->
    infoBubbleText="" <!-- notification presented in the Problem blade when an issue is found -->
	service="Microsoft.Kusto" <!-- name of the resource provider in ARM -->
	resource="clusters" <!-- ARM Name of the resource type -->
	authors="kustosee"
    ms.author="prvavill"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32613464,32613482,32613506"
	resourceTags=""
	productPesIds="16602"
	cloudEnvironments="Public"
    articleId="67CED318-3125-4546-BA44-FB23E224CC15"
	ownershipId="AzureDataExplorer_Kusto"
/>

# Azure Data Explorer query failures

## **Recommended Documents**

### Error E_LOW_MEMORY_CONDITION: Operation was aborted due to available process memory running low

-  Your Azure Data Explorer is having query failures with low memory issues and query failures due to low memory are result of a non-optimized workload running against your Azure Data Explorer. Possible recommendations to follow query best practises using [this reference](https://docs.microsoft.com/azure/kusto/query/best-practices) or consider adding more power using [this reference](https://docs.microsoft.com/azure/data-explorer/manage-cluster-horizontal-scaling) if required following [this reference](https://docs.microsoft.com/azure/data-explorer/using-metrics). 
