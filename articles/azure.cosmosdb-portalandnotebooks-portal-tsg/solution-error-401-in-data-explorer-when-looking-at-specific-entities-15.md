<properties
	  pageTitle="Error 401 in data explorer when looking at specific entities"
	  description="Error 401 in data explorer when looking at specific entities"
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
	  articleId="54e21eea-7df0-40ce-a40d-5d62a3b8632d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Error 401 in data explorer when looking at specific entities

<!--issueDescription-->

Dear customer,

URL escaped characters such as % are not supported in IDs.

Every resource within an Azure Cosmos DB database account needs to have a unique identifier. Unlike ResourceId, which is set internally, this Id is settable by the user and is not immutable. When working with document resources, they too have this settable Id property. If an Id is not supplied by the user the SDK will automatically generate a new GUID and assign its value to this property before persisting the document in the database. You can override this auto Id generation by setting the disableAutomaticIdGeneration parameter on the DocumentClient instance to true. This will prevent the SDK from generating new Ids.
 

The following characters are restricted and cannot be used in the Id property: '/', '\', '?', '#'

Thank you.

<!--/issueDescription-->

