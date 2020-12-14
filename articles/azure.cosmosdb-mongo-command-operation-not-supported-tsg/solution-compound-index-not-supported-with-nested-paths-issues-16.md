<properties
	  pageTitle="Compound index not supported with nested paths issues"
	  description="Compound index not supported with nested paths issues"
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
	  articleId="6ff6018f-5086-4559-8907-7fecce0cdcda"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Compound index not supported with nested paths issues

<!--issueDescription-->

Please confirm that no arrays are in the path then transfer to PG to enable config. 

**Customer message:**
Dear customer,

If you are getting the error below:
```
globaldb:PRIMARY> db.test.createIndex({a:1,"c.d":1})
{
        "ok" : 0,
        "errmsg" : "Compound index does not currently support nested documents or arrays.",
        "code" : 115,
        "codeName" : "CommandNotSupported"
}
```

###Cause
Please be aware that we currently do not support nested documents or arrays.  
https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-indexing#index-types  

###Mitigation
?	Please confirm that no arrays are in the path.  
?	Refactor data model to bring field to root.  

Thank you .

<!--/issueDescription-->
