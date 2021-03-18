<properties
	  pageTitle="ARM ACL deny permission restricting portal to get Cosmos DB key"
	  description="ARM ACL deny permission restricting portal to get Cosmos DB key"
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
	  articleId="9baa2921-4496-460a-ae1e-66bb29b7cea2"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# ARM ACL deny permission restricting portal to get Cosmos DB key

<!--issueDescription-->

Dear customer, 

In case you are unable to access the Cosmos  DB in Portal or Cosmos DB Portal Overview page fails with Access Denied, i.e., the user is the owner of the Cosmos DB Account or does have full control permission but  still the below exception is shown in the portal.

See this [image](https://microsofteur-my.sharepoint.com/:f:/g/personal/anferrei_microsoft_com/Ejtoj2C2Ur5CnQLPyCHlgjgBkOw42vGQN3SpjyTquCcN7g?e=nVqovx).

ARM have released a feature called ?Blue Print? which basically helps to ACL a deny permission. This feature is basically restricting the portal to get the Cosmos DB key.

Quick way to Confirm ARM issue: you can run the Azure CLI and if the keys are not shown then the arm is not returning the keys due to the ACL from Blue Print.
`
az cosmosdb list-read-only-keys --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup
`

###Example  
`
az cosmosdb list-read-only-keys --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup
`

##Mitigation
- you can use the sunset link (https://cosmos.azure.com/) if you have connection string for cosmosdb account.  
or
- You need to remove the Deny by removing configuration through Blue Print.

Thank you.

<!--/issueDescription-->

