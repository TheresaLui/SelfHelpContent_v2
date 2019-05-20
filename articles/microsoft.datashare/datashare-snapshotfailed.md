<properties
	pageTitle="Why did snapshot fail?"
	description="Why did snapshot fail?"
	service="Microsoft.DataShare"
	resource="accounts"
	authors="mkadiri3"
	ms.author="makadiri"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="1d423bf5-f0a3-48fc-a6a1-314e04ea791f"
/>

# Why did snapshot fail?

The Azure Data Share service requires permission to the target storage account on the Data Consumer side in order for data to be copied successfully. Once the Data Consumer specifies a storage account, it can take a few minutes for the appropriate permission to propagate over to the storage account. In this event, the following steps are recommended:

## **Recommended Steps**

* In this event, Data Consumer should wait approximately 5-10 minutes before re-running the snapshot.
