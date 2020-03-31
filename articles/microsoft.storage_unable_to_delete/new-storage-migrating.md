<properties
	pageTitle="Storage account is in the process of migrating"
	description="Storage account is in the process of migrating"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32602738"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="5a2a90e9-4bfc-4e4b-9077-b1c71ceb042d"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage account is in the process of migrating

1. This error usually occurs when a customer started a migration from Classic to ARM and did not perform the commit operation.
2. In this specific cases, an ASM to ARM migration seems to be in progress for the customer's Storage Account. Follow the next steps to unblock the customer to being able to delete the desired Storage Account.
    1. First, customer can perform a Commit operation for the migration process to be completed:

~~~powershell

Move-AzureStorageAccount-Commit -StorageAccountName storageAccountName -Debug

~~~
   3. If the Commit operation failed for any reason they can also Abort the migration by executing the command:

~~~powershell

Move-AzureStorageAccount-Abort -StorageAccountName storageAccountName -Debug

~~~

**Recommended Documents**

1. https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265688/Azure_Storage_TSG_Storage-account-is-in-the-process-of-being-migrated-and-hence-cannot-be-changed(StorageAccou


