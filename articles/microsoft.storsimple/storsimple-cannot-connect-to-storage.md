<properties
	pageTitle="Cannot connect to storage account"
	description="Cannot connect to storage account"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="802e229d-5a5b-4d09-af3d-2ba65b139eb5"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630495"
	resourceTags="8000Series"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Cannot connect to storage account 

## **Recommended Steps**

1. Verify if the access key to storage account has been regenerated and if so, synchronize the access key of your storage account [by following these instructions](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-storage-accounts#to-synchronize-keys-for-storage-accounts-in-the-same-subscription-as-the-service).
2. [Verify if Azure Datacenter IP address is whitelisted to allow traffic to Azure Storage](https://www.microsoft.com/download/confirmation.aspx?id=41653)
3. [Run network diagnostics to check if the Storage account credentials and SSL certificate is valid](https://docs.microsoft.com/azure/storsimple/storsimple-8000-diagnostics#to-run-the-diagnostics-tool)
