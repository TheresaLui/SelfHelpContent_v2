<properties
	  pageTitle="Invalid characters in Resource id rid Property"
	  description="Invalid characters in Resource id rid Property"
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
	  articleId="c292d3f5-121b-41dd-8cc5-92a3c7dc585a"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Invalid characters in Resource.Id _rid Property

<!--issueDescription-->

Dear customer,

Get request returns a bad request error may be given if the resource Id , _rid , property contains invalid characters.  
* The following characters are restricted and cannot be used in the Id property: */*, *\\*, *?*, *#* 
* Please see reference [Resource.Id Property](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.resource.id?view=azure-dotnet#remarks) 

Thank you.

<!--/issueDescription-->

