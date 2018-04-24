<properties
	pageTitle="Metadata operations RCA"
	description="RCA - High number of metadata operations on collection"
	infoBubbleText="Found information related to Machine Key Status. See details on the right."
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="metadatacritical_43DFF466-CDE2-4319-95F7-92FF92B302A4"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found a high number of metadata operations on your account
<!--/issueDescription-->
The large number of metadata operations can possibly arise due to multiple initializations of the DocumentClient object which retrieves informations about the account and its collections. It is recommended to cache and reuse this instance within your application rather than creating a new instance for each operations. Please refer this [link](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.documentclient?view=azure-dotnet#remarks) for more details.
