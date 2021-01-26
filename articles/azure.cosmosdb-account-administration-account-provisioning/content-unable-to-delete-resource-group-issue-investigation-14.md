<properties
	  pageTitle="Unable to delete Resource Group issue investigation"
	  description="Unable to delete Resource Group issue investigation"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="9e74d0e3-2a18-4a45-90f9-e115b8fdeff7"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Unable to delete Resource Group issue investigation

The customer was not able to Delete the resource Group. This TSG will provide details on how to check for failures with ARM operations.

<br>

This Kusto should be executed on ARMProd connection:
https://armprod.kusto.windows.net/ARMProd 


<br>

```
EventServiceEntries
| where subscriptionId == "070a6cfa-cd3c-407e-8752-5ab7df13b16b"
| where resourceUri contains "graph-test" //the resource name (for Cosmos DB:database account name)
//| where status == "Failed"
| where TIMESTAMP > ago(1d) 
| where operationName == "Microsoft.DocumentDB/databaseAccounts/delete" //Depends on the ARM resource provider operation
```

