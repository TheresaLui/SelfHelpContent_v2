<properties
	pageTitle="Azure Backup - I am having issues configuring or enabling backup"
	description="Azure Backup - I am having issues configuring or enabling backup"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637322"
	resourceTags=""
	productPesIds="15571,15797,16470,16454,14749"
	articleId="9ba9becb-d7a2-4b16-b471-3cfd6ed0570a"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup - I am having issues configuring or enabling backup

## **Recommended Steps**

* [UserErrorGuestAgentStatusUnavailable](https://aka.ms/AB-AA4ecq8) - VM agent unable to communicate with Azure Backup<br>
* [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress ](https://aka.ms/AB-AA4e56y)- Unable to initiate backup as another backup operation is currently in progress<br>
* [UserErrorUnsupportedDiskSize](https://aka.ms/AB-AA4ecqf) - Currently Azure Backup does not support disk sizes greater than 4095GB<br>
* [ExtensionSnapshotFailedNoNetwork](https://aka.ms/AB-AA4ecqk) - Snapshot operation failed due to no network connectivity on the virtual machine<br>
* [GuestAgentSnapshotTaskStatusError](https://aka.ms/AB-AA4e56x) - Could not communicate with the VM agent for snapshot status<br>
* [UserErrorRpCollectionLimitReached](https://aka.ms/AB-AA4e56l) - The Restore Point collection max limit has reached<br>
* [UserErrorKeyvaultPermissionNotConfigured](https://aka.ms/AB-AA4e56m) - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs<br>
* [ExtentionOperationFailed](https://aka.ms/AB-AA4e56c) - VMSnapshot extension operation failed<br>
* [BackUpOperationFailed / BackUpOperationFailedV2](https://aka.ms/AB-AA4ecqe) - Backup fails, with an internal error<br>

## **Recommended Documents**

* [Azure Virtual Machine backup troubleshooting guide](https://aka.ms/AB-AA4ecqg)<br>
* [Configure Azure VMs Backup in Recovery Services vault](https://aka.ms/AB-AA4ecq2)<br>
* [Enable Backup during VM creation](https://aka.ms/AB-EnableBackupDuringVMcreation)<br>
* [Enable Backup from VM blade](https://aka.ms/AB-EnableBackupDuringVMcreation)<br>
* [Restore VM](https://aka.ms/AB-AA4e568)<br>
* [Restore files from VM backup](https://aka.ms/AB-AA4e56h)<br>
* [Restore VM to alternate location](https://aka.ms/AB-AA4e570)<br>
* [Create VM from restored disks](https://aka.ms/AB-AA4e56j)<br>
* [Configure](https://aka.ms/AB-backupReorts) and [view](https://aka.ms/View-PowerBI-Report) Backup report using Power BI<br>
* Monitor [Alerts and Jobs](https://aka.ms/Monitor-JobsAlert-RSV) through Recovery Services vault<br>
* [Configure Notifications](https://aka.ms/Configure-Notification-RSV) for backup Alerts through Recovery Services vault<br>
* [Monitor Azure Backup](https://aka.ms/Monitor-Backup-LA) and [create Alerts](https://aka.ms/Create-Alert-LA) using Log Analytics<br>
* [Stop protecting virtual machines](https://aka.ms/AB-AA4ecqs)<br>
* [Delete Backup data](https://aka.ms/AB-AA4e56f)<br>
* [Delete Recovery Services vault](https://aka.ms/AB-AA4ecq5)
