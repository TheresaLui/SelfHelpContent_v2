<properties
	pageTitle="Move data to the new storage account"
	description="Move data to the new storage account"
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
	articleId="2cd788f2-f73f-4259-9e4c-5d6f3258f659"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Move data to the new storage account 

Here's some ways to move your data over 

1. Azure Storage Explorer : It's easy-to-use, and suitable for small data sets. You can copy containers and file shares, and then paste them into the target account. 
2. AzCopy: This is the preferred approach. It's optimized for performance. One way that it's faster, is that data is copied directly between storage servers, so AzCopy doesn't use the network bandwidth of your computer. Use AzCopy at the command line or as part of a custom script. 
3. Azure Data Factory: Use this tool only if you need functionality that isn't supported in the current release of AzCopy. For example, in the current release of AzCopy, you can't copy blobs between accounts that have a hierarchical namespace. Also AzCopy doesn't preserve file access control lists or file timestamps (For example: create and modified time stamps). 
