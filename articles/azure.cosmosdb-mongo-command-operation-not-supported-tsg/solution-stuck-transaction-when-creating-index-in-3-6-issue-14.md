<properties
	  pageTitle="Stuck transaction when creating index in 3.6 issue"
	  description="Stuck transaction when creating index in 3.6 issue"
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
	  articleId="fd9aac71-c9e8-4fed-997e-bdbe564b2b2e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Stuck transaction when creating index in 3.6 issue

<!--issueDescription-->

Dear customer,

When you try to create an index, it pops with below error
```
db.test.createIndex({b:1})
{
        "ok" : 0.0,
        "errmsg" : "[ActivityId=<>] Detected stuck collection metadata for <Collection Name>",
        "code" : 1.0,
        "codeName" : "InternalError"
}
```
Or below error:
```
db.test.createIndex({b:1})
{
        "ok" : 0.0,
        "errmsg" : "[ActivityId=<>] Internal error.",
        "code" : 1.0,
        "codeName" : "InternalError"
}
```

#### Cause
The cause of the issue is because you added unique index while documents existed in the collection.  

#### Solution
Please use the following command: db.coll.reIndex()

Thank you .

<!--/issueDescription-->

