<properties
	pageTitle="Check if the source storage account use any preview features enabled"
	description="Check if the source storage account use any preview features enabled"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9be7b3f9-f583-4d34-9435-197b519c5a41"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if the source storage account use any preview features enabled

Storage account can have preview features on. This features will vary depending on time when we are checking. You can check various ways, features on a storage account.

1. Check using [Jarvis actions](https://jarvis-west.dc.ad.msft.net/5FC2DD56?genevatraceguid=fe06b159-0895-4052-bca2-d974934225c3). 
2. Check in ASC (Storage Account --> Summary Tab --> Configurations). 
3. Things to check if the source account features will be available in target region. (account type, kind LRS, RAGRS, ZRS, ADLS Gen2, Large File Share, ...)

To check the current preview features valid for azure storage, visit [Azure Updates](https://azure.microsoft.com/en-us/updates/?status=inpreview&category=storage)

