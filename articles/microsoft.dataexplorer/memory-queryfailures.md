<properties
	pageTitle="Performance|Low memory query failures"
	description="Query failures with low memory"
    infoBubbleText="Query failures with low memory"
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
    articleId="616C3687-5C8A-4920-A01A-47D2E321AC3E"
	ownershipId="AzureDataExplorer_Kusto"
/>

# Azure Data Explorer query failures

<!--issueDescription-->
Your Azure Data Explorer is having query failures with LOW MEMORY CONDITION issues and query failures due to low memory are result of a non-optimized workload running against your Azure Data Explorer. Low memory query failures can also occur if the cluster is running high (above 81%) in data capacity or cluster is running queries with high CPU usage (95%). 
<!--/issueDescription-->

## **Recommended Documents**

- Possible recommendations to follow our [query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices) or consider adding more power by [scaling out your cluster](https://docs.microsoft.com/azure/data-explorer/manage-cluster-horizontal-scaling) or monitor your performance using [metrics](https://docs.microsoft.com/azure/data-explorer/using-metrics)
