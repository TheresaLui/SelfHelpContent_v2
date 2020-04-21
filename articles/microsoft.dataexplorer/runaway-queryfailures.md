<properties
	pageTitle="Performance|Runaway query failures"
	description="Performance|Runaway query failures"
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

### Error E_RUNAWAY_QUERY: Query execution aborted as it exceeded its allowed resources

- Your Azure Data Explorer is having runaway query failures and it is a kind of partial query failure that happens when some internal query limit was exceeded during query execution. Use [this reference](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/runawayqueries) to assist in possible courses of action to avoid these errors. 
