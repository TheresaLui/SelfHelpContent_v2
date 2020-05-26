<properties
	pageTitle="Performance|Resultset Large query failures"
	description="Resultset Large query failures"
    infoBubbleText="Resultset Large query failures"
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
	cloudEnvironments="Public, fairfax, usnat, ussec"
    articleId="862E4B9B-7E83-4FB1-97FA-2D62605245B7"
	ownershipId="AzureDataExplorer_Kusto"
/>

# Azure Data Explorer query failures

<!--issueDescription-->
Your Azure Data Explorer is having query result set has exceeded the internal limit failures and it is a partial query failure that happens when the query's result has exceeded a limit on the number of records or a limit on the total amount of data.  
<!--/issueDescription-->

## **Recommended Documents**

- Follow [result truncation concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/resulttruncation) to assist in possible courses of action to avoid these errors

