<properties
	pageTitle="Performance|Low memory query failures"
	description="Performance|Low memory query failures"
    infoBubbleText=""
	service="Microsoft.Kusto"
	resource="clusters"
	authors="radennis"
    ms.author="prvavill"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
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
