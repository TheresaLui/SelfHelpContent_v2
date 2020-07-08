<properties
	pageTitle="Unable to delete vault"
	description="Issue with delete vault due to items protected"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="akgoyal"
	ms.author="akgoyal"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId= "6F401FC2-342B-437B-84A8-C4F43B28C017"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issue with delete vault 

**These are the Protected items in the vault that are blocking the delete operation:**
<!--issueDescription-->
IaaSVM : <!--IaaSVM-->IaaSVM<!--/IaaSVM-->

Azure Workload : <!--AzureWorkload-->AzureWorkload<!--/AzureWorkload-->

Azure Storage : <!--AzureStorage-->AzureStorage<!--/AzureStorage-->

DPM : <!--DPM-->DPM<!--/DPM-->

Azure Backup Server : <!--AzureBackupServer-->AzureBackupServer<!--/AzureBackupServer-->

MAB : <!--MAB-->MAB<!--/MAB--> 

<!--/issueDescription-->

## **Recommended Steps**

* You can't delete a Recovery Services vault with any of the following dependencies:
  
  * Vault contains protected data sources (for example, IaaS VMs, SQL databases, Azure file shares, etc.)
  * Vault contains backup data. Once backup data is deleted, it will go into the soft deleted state.
  * Vault contains backup data in the soft deleted state  
  
* For **step-by-step instructions to permanently delete vault** refer to this [article](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault)