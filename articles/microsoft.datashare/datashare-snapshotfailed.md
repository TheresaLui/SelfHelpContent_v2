<properties
	pageTitle="Why did my snapshot fail?"
	description="Why did my snapshot fail?"
	service="Microsoft.DataShare"
	resource="accounts"
	authors="joannapea"
	ms.author="joanpo"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32675627,32675629"
	resourceTags=""
	productPesIds="16762"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="1d423bf5-f0a3-48fc-a6a1-314e04ea791f"
	ownershipId="AzureData_DataShare"
/>

# Why did my snapshot fail?

The Azure Data Share service requires permission to the target storage account on the Data Consumer side in order for data to be copied successfully. Once the Data Consumer specifies a storage account, it can take a few minutes for the appropriate permission to propagate over to the storage account.

## **Recommended Steps**

* In this event, the Data Consumer should wait approximately 5-10 minutes before re-running the snapshot
