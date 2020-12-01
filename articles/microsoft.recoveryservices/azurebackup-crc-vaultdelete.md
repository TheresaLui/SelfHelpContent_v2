<properties
    pageTitle="Unable to delete vault"
	description="Issue with delete vault due to items protected"
    infoBubbleText="Protected items exist"
    service="microsoft.recoveryservices"
    resource="backup"
    authors="akgoyal"
    ms.author="akgoyal"
    displayOrder=""
    articleId= "6F401FC2-342B-437B-84A8-C4F43B28C017"
    diagnosticScenario="azurebackup-crc-vaultdelete"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issue with delete vault 

<!--issueDescription-->
Our internal service telemetry detected that your vault **<!--$VaultName-->VaultName<!--/$VaultName-->** contains Protected Items. Vault deletion is blocked until these items are deleted.
<!--/issueDescription-->

* Azure Virtual Machine: **<!--$IaaSVM-->IaaSVM<!--/$IaaSVM-->**
* SAP HANA in Azure VM: **<!--$SAPHanaDatabase-->SAPHanaDatabase<!--/$SAPHanaDatabase-->**
* SQL in Azure VM: **<!--$SQLDataBase-->SQLDataBase<!--/$SQLDataBase-->**
* Azure Storage(Azure Files): **<!--$AzureStorage-->AzureStorage<!--/$AzureStorage-->**
* DPM: **<!--$DPM-->DPM<!--/$DPM-->**
* Azure Backup Server: **<!--$AzureBackupServer-->AzureBackupServer<!--/$AzureBackupServer-->**
* Azure Backup Agent: **<!--$MAB-->MAB<!--/$MAB-->**

## **Recommended Steps**

* You can't delete a Recovery Services vault with any of the following dependencies:
  
  * Vault contains protected data sources (for example, IaaS VMs, SQL databases, Azure file shares, etc.)
  * Vault contains backup data. Once backup data is deleted, it will go into the soft deleted state.
  * Vault contains backup data in the soft deleted state  
  
* For **step-by-step instructions to permanently delete vault** refer to this [article](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault)