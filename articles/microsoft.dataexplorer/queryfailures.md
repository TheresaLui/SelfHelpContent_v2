<properties
	pageTitle="Performance|Kusto query failures"
	description="Performance|Kusto query failures"
    infoBubbleText=""
	service="Microsoft.Kusto"
	resource="clusters"
	authors="radennis"
    ms.author="prvavill"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32613464,32613482,32613506"
	productPesIds="16602"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    articleId="66BF4592-B7E3-4820-AA25-E6BC77A179AE"
	ownershipId="AzureDataExplorer_Kusto"
/>

# Azure Data Explorer query failures

Information about specific Azure Data Explorer error codes for query failures can be found [here](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/errorsinnativecode). Information about troubleshooting specific common errors is given below.

## **Recommended Documents**

### Error E_QUERY_RESULT_SET_TOO_LARGE: The result set for this query exceed its allowed record/size limits

- A query result set has exceeded the internal ... limit is a partial query failure that happens when the query's result has exceeded a limit on the number of records (default 500,000) or a limit on the total amount of data (default 67,108,864 (64MB). Follow [result truncation concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/resulttruncation) to assist in possible courses of action to avoid these errors. 

### Error E_RUNAWAY_QUERY: Query execution aborted as it exceeded its allowed resources

- A runaway query is a partial query failure that happens when some internal query limit was exceeded during query execution. Follow [runaway queries concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/runawayqueries) to assist in possible courses of action to avoid these errors. 

### Error E_ENTITY_NOT_FOUND: The requested entity was not found

- Database or table referenced in query does not exist in the Azure Data Explorer cluster. [Create database](https://docs.microsoft.com/azure/data-explorer/create-cluster-database-portal) and [create table](https://docs.microsoft.com/azure/data-explorer/kusto/management/tables) to avoid this error.

### Error E_OVERFLOW: Represents an arithmetic overflow error (the result of a computation is too large for the destination type)

- An overflow occurs when the result of a computation is too large for the destination type. This phenomenon usually leads to a partial query failure. Follow [overflow concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/overflow) to assist in possible courses of action to avoid these errors. 

### Error E_LOW_MEMORY_CONDITION: Operation was aborted due to available process memory running low

-  Query failures due to low memory are result of a non-optimized workload running against your Azure Data Explorer. Possible recommendations to follow our [query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices) or consider adding more power by [scaling out your cluster](https://docs.microsoft.com/azure/data-explorer/manage-cluster-horizontal-scaling) or monitor your performance using [metrics](https://docs.microsoft.com/azure/data-explorer/using-metrics). 
