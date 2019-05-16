<properties
	pageTitle="Why did snapshot fail?"
	description="Why did snapshot fail?"
	service="Microsoft.DataShare"
	resource="accounts"
	authors="joannapea"
	ms.author="joanpo"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="be646d3e-d5cb-41ba-84eb-328e2f2fa6ed"
/>

# Why did snapshot fail?

The Azure Data Share service requires permission to the target storage account on the Data Consumer side in order for data to be copied successfully. Once the Data Consumer specifies a storage account, it can take a few minutes for the appropriate permission to propagate over to the storage account. In this event, the following steps are recommended:

## **Recommended Steps**

* In this event, Data Consumer should wait approximately 5-10 minutes before re-running the snapshot.
