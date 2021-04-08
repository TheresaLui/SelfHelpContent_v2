<properties
  pagetitle="Azure Data Explorer query failures&#xD;"
  description="Performance|Kusto query failures"
  service="microsoft.kusto"
  resource="clusters"
  ms.author="prvavill,dagrawal"
  selfhelptype="Resource"
  supporttopicids="32613464,32613482,32613506,32786222,32786228,32786229,32786230,32786231"
  resourcetags=""
  productpesids="16602"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="66bf4592-b7e3-4820-aa25-e6bc77a179ae"
  ownershipid="AzureDataExplorer_Kusto" />
# Azure Data Explorer query failures

If you're have query failure in Azure Data Explorer, refer to this document on [specific error codes](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/errorsinnativecode). For more information about troubleshooting specific common errors, refer to the next section. 

## **Recommended Documents**

### Error E_QUERY_RESULT_SET_TOO_LARGE: The result set for this query exceed its allowed record/size limits

This error indicates a partial query failure caused by the result set exceeding a limit. Limits can be set on the number of records (default 500,000) or the total amount of data (default 67,108,864 (64MB). Follow [result truncation concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/resulttruncation) to assist in possible courses of action to avoid these errors. 

### Error E_RUNAWAY_QUERY: Query execution aborted as it exceeded its allowed resources

A runaway query is a partial query failure that happens when an internal query limit was exceeded during query execution. Follow [runaway queries concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/runawayqueries) to assist in possible courses of action to avoid these errors. 

### Error E_ENTITY_NOT_FOUND: The requested entity was not found

The database or table referenced in the query does not exist in the Azure Data Explorer cluster. See [Create database](https://docs.microsoft.com/azure/data-explorer/create-cluster-database-portal) and [create table](https://docs.microsoft.com/azure/data-explorer/kusto/management/tables) to avoid this error.

### Error E_OVERFLOW: Represents an arithmetic overflow error (the result of a computation is too large for the destination type)

An overflow occurs when the result of a computation is too large for the destination type. This phenomenon usually leads to a partial query failure. Follow [overflow concepts](https://docs.microsoft.com/azure/data-explorer/kusto/concepts/overflow) to assist in possible courses of action to avoid these errors. 

### Error E_LOW_MEMORY_CONDITION: Operation was aborted due to available process memory running low

Query failures due to low memory are the result of a non-optimized workload running against your Azure Data Explorer. Possible recommendations include:
- Follow our [query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices)
- Consider adding more power by [scaling out your cluster](https://docs.microsoft.com/azure/data-explorer/manage-cluster-horizontal-scaling) 
- Monitor your performance using [metrics](https://docs.microsoft.com/azure/data-explorer/using-metrics)
