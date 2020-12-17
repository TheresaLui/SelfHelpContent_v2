<properties
	  pageTitle="ARM ACL deny permission restricting the portal to get Cosmos DB key"
	  description="ARM ACL deny permission restricting the portal to get Cosmos DB key"
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
	  articleId="608d04d6-12e7-42c7-bee8-18ca2ffbb11e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# ARM ACL deny permission restricting the portal to get Cosmos DB key

Unable to access the Cosmos  DB in Portal or Cosmos DB Portal Overview page fails with Access Denied

The user is the owner of the Cosmos DB Account or does have full control permission.  But still the below exception is shown in the portal. 

Symptom, see this [image](https://microsofteur-my.sharepoint.com/:f:/g/personal/anferrei_microsoft_com/Ejtoj2C2Ur5CnQLPyCHlgjgBkOw42vGQN3SpjyTquCcN7g?e=nVqovx).

ARM have released a feature called ?Blue Print? which basically helps to ACL a deny permission. This feature is basically restricting the portal to get the Cosmos DB key.

You can confirm that the ARM is causing the issue by Query in ARM Prod Kuto endpoint. Any result from the query does indicate that the Blue Print/ARM is causing this issue.

```
Traces
| where TIMESTAMP > ago(1d)
| where operationName == "AuthorizationFilterEngine.FilterResourcesByDenyAssignment"
| where message startswith "Received '0' resources. Returning '0' resources after filtering by deny assignment. Orignial groups count"
| where subscriptionId =="78009f05-82b1-4921-8b77-5b05aa892d1c"
| project TIMESTAMP, ActivityId, subscriptionId, operationName,message
| limit 10
```

###Quick way to Confirm ARM issue
You can run the Azure CLI and if the keys are not shown then the arm is not returning the keys due to the ACL from Blue Print.
`
az cosmosdb list-read-only-keys --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup
`

###Example  
`
az cosmosdb list-read-only-keys --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup
`

##Mitigation
- Customer can use the sunset link if they have connection string for cosmosdb account.  
or
- They need to remove the Deny by removing configuration through Blue Print.

