<properties
	  pageTitle="NotSupportedMongoException: 'unique' is not supported issue"
	  description="NotSupportedMongoException: 'unique' is not supported issue"
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
	  articleId="9e5686fb-5ed0-465b-b225-e86afaecf53a"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# NotSupportedMongoException: 'unique' is not supported issue

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **
If the following steps don't help the customer, please create a CRI for Product team to enable if needed.

## Customer message:
Dear customer,

**Error message returned**
`
Microsoft.Azure.Documents.Interop.Mongo.Exceptions.NotSupportedMongoException: 'unique' is not supported
`

CosmosDB now supports  index management + Unique indexes on CosmosDB -  Mongo accounts in private preview.   We enable this config on all the customer accounts by setting the below naming service configuration

|Description|Naming config to enable|Value to set|
|-|-|-|
|Mongo index management/Mongo unique index|enableMongoIndexManagement|True|


MongoDB supports extended bson types like (DateTime/ ISODate/ Timestamp/ Symbol / Binary).  To enable unique indexes on such types, the customers account needs to be in the new bson schema.

To validate, you need to run 'get database account'  ACIS command against the account and check for the highlighted configuration override in the output.

```
      },
      "configurationOverrides": {
        "enableBsonSchema": "True"
      }
    }
```
 

If enableBsonSchema is false and/or  is set to true, follow the guidelines for enabling bson schema on the account before enabling index management

<!--/issueDescription-->

