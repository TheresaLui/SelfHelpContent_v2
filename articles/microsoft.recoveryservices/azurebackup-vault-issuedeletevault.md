<properties
	pageTitle="Unable to delete vault"
	description="Issue with delete vault"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632791"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ac99254c-7320-4261-8c2b-3bea2a1a0022"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issue with delete vault

## **Recommended Documents**
* You can't delete a Recovery Services vault with any of the following dependencies:
  * You can't delete a vault that contains protected data sources (for example, IaaS VMs, SQL databases, Azure file shares, etc.)
  * You can't delete a vault that contains backup data. Once backup data is deleted, it will go into the soft deleted state.
  * You can't delete a vault that contains backup data in the soft deleted state.
  * You can't delete a vault that has registered storage accounts.
* For **step-by-step instructions to permanently delete vault** refer this [article](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault).
