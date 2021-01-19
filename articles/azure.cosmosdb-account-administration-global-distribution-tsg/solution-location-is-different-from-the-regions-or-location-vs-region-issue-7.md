<properties
	  pageTitle="Location is different from the Regions or Location vs Region issue"
	  description="Location is different from the Regions or Location vs Region issue"
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
	  articleId="add372ab-e2a9-4666-a9de-b4d20cd02df8"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Location is different from the Regions or Location vs Region issue

<!--issueDescription-->

Dear customer,

The Azure portal shows the location information as show below. This location is a property is exportedby the Azure ARM which is based on the location the Cosmos DB Resource was created

See [image](https://microsofteur-my.sharepoint.com/:f:/g/personal/anferrei_microsoft_com/EjtUQ8_8HE1Jmuxfyl94XkkB4Bd-iJW4KscZaI0iMz7lsw?e=ze4C3k)

However, the location property is not the same as the Cosmos DB Region property shown in the Cosmos DB overview page or in the Geo-replication tab in the Azure portal. 

The  Cosmos DB Region indicates the regions where  the actual data is located.  The ARM location property does not have anything to do with the region the data is located. Also, this information cannot be updated or changed.

Please take into account that there is not impact of having this location completely different from the Cosmos DB Regions.

Thank you.

<!--/issueDescription-->

