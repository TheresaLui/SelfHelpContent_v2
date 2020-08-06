<properties
	pageTitle="UserErrorBCMPremiumStorageQuotaError"
	description="UserErrorBCMPremiumStorageQuotaError"
	infoBubbleText="Could not copy the snapshot of the virtual machine, due to insufficient free space in the storage account."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
  ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbcmpremiumstoragequotaerror"
	diagnosticScenario="azurebackup-crc-usererrorbcmpremiumstoragequotaerror"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277,32553285"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# I received error "UserErrorBCMPremiumStorageQuotaError"

<!--issueDescription-->
We identified that your backup operation failed due to insufficient space in the premium storage account. The snapshot of the virtual machine could not be copied.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the UserErrorBCMPremiumStorageQuotaError issue, perform the below steps:

* Ensure that storage account has free space equivalent to the data size in the premium disks attached to the Virtual Machines
* To check the size of the premium storage account, perform the below:

    * Sign in to Azure Portal, go to **Storage accounts**, select the storage account in which the failed backup VM resides
    * Click **Metrics** option in the **Monitoring** section
    * Select **Used capacity** in the **Metrics** drop-down option to check the used capacity of storage account
    * Retry your Backup operation

## **Recommended Documents**

* [Storage account free space requirements](https://azure.microsoft.com/documentation/articles/backup-introduction-to-azure-backup/#back-up-and-restore-premium-storage-vms)
