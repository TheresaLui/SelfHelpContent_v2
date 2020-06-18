<properties
	pageTitle="Managed Disk Recovery"
	description="Managed Disk Recovery"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="6cc2a6b9-23e5-4566-8180-a33bc5834ac6"
/>

# Managed Disk Recovery

Azure Storage Manage disks are generally not recoverable. Please check if customer has snapshots or any other backup. If present they can copy data out from the snapshot using storage explorer as follows:

1. Evaluate with the customer the exact subscription id / resource group /manage disk name / time window of the operation
2. A manage disk is always within a storage account
3. Note: As part of our data privacy guarantee, we ensure that data deleted by our customer is eventually overwritten. 
4. This storage account and all its content may not be recoverable by Azure even when all conditions above are true.
