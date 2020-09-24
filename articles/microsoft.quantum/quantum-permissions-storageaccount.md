<properties
	pageTitle="Permission denied accessing job input or output data"
	description="When you attempt to write the input data for a job or read the output data for a job you receive a permission denied (403 Forbidden) error"
	infoBubbleText="Permission issues when reading input or output data"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="mblouin"
	displayOrder="2"
	articleId="quantum-permissions-storageaccount"
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds="32740179,32740177,32740184,32740193,32740191,32740190,32740182"
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Azure_Quantum"
/>

# Permission denied accessing job input or output data

Job input and output data is stored in an Azure Storage account deployed in the same subscription as your workspace. This storage account is associated with the Quantum Workspace at creation time.

As the storage account remains a separate resource you may experience various types of permission issues trying to access it.


## **Recommended Steps**

1. Review the input and output data links on the job that you are trying to access. They contain the storage account name as part of the URL.
2. Review the permission settings on the storage account.
3. To reconfigure permissions, please follow the documentation around [storage account permissions](https://docs.microsoft.com/azure/storage/common/storage-access-blobs-queues-portal)

## **Recommended Documents**

* [Storage account permissions](https://docs.microsoft.com/azure/storage/common/storage-access-blobs-queues-portal)
