<properties
	pageTitle="Performance|Resultset Large query failures"
	description="Performance|Resultset Large query failures"
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

### Error E_QUERY_RESULT_SET_TOO_LARGE: The result set for this query exceed its allowed record/size limits

- Your Azure Data Explorer is having query result set has exceeded the internal ... limit failures and it is a kind of partial query failure that happens when the query's result has exceeded a limit on the number of records (default 500,000) or a limit on the total amount of data (default 67,108,864 (64MB). Use [this reference](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/resulttruncation) to assist in possible courses of action to avoid these errors. 

