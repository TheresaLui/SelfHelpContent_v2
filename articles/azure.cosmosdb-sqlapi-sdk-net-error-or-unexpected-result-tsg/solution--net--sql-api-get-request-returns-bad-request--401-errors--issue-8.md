<properties
	  pageTitle=".Net: SQL API Get Request Returns Bad Request (401 Errors) issue"
	  description=".Net: SQL API Get Request Returns Bad Request (401 Errors) issue"
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
	  articleId="0786ded9-23eb-4c48-8c74-1ce4a300ddfc"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# .Net: SQL API Get Request Returns Bad Request (401 Errors) issue

<!--issueDescription-->

Dear customer,

A Get request returns a bad request error may be given if the resource Id , _rid , property contains invalid characters. 

Please see the document: 
https://docs.microsoft.com/en-us/dotnet/api/microsoft.azure.documents.resource.id?view=azure-dotnet#remarks

Every resource within an Azure Cosmos DB database account needs to have a unique identifier. Unlike ResourceId, which is set internally, this Id is settable by the user and is not immutable. When working with document resources, they too have this settable Id property. If an Id is not supplied by the user the SDK will automatically generate a new GUID and assign its value to this property before persisting the document in the database. You can override this auto Id generation by setting the disableAutomaticIdGeneration parameter on the DocumentClient instance to true. This will prevent the SDK from generating new Ids.

The following characters are restricted and cannot be used in the Id property: '/', '\', '?', '#'

Thank you.

<!--/issueDescription-->

