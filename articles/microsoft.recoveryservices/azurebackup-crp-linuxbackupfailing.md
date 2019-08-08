<properties
	pageTitle="Backup of Azure virtual machine fails"
	description="Backup of Azure virtual machine fails"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32637320"
	resourceTags="linux,redhat,ubuntu"
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public"
	articleId="ce3059e1-dea9-432e-8d74-f16235e18dd6"
/>

# Azure Backup - Backup is failing for my VM

## **Recommended Steps**

* [Ensure your Linux VM agent is up to date before troubleshooting further](https://aka.ms/AB-AA4ecq9)<br>
* [Ensure there is connectivity between VM and Azure Storage endpoints](https://aka.ms/AB-AA4ecqy)<br>
* [If your Linux OS/Kernel version is not listed here, then it is not supported](https://aka.ms/AB-AA4ecr1)<br>
* [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://aka.ms/AB-AA4ecq1)<br>
* [If your issue is still not resolved, check VM Backup troubleshooting guide](https://aka.ms/AB-AA4ecq1)<br>

## **Recommended Documents**

* [UserErrorGuestAgentStatusUnavailable](https://aka.ms/AB-AA4ecq8) - VM agent unable to communicate with Azure Backup<br>
* [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress](https://aka.ms/AB-AA4e56y) - Unable to initiate backup as another backup operation is currently in progress<br>
* [UserErrorUnsupportedDiskSize](https://aka.ms/AB-AA4ecqf) - Currently Azure Backup does not support disk sizes greater than 4095GB<br>
* [ExtensionSnapshotFailedNoNetwork](https://aka.ms/AB-AA4ecqk) - Snapshot operation failed due to no network connectivity on the virtual machine<br>
* [GuestAgentSnapshotTaskStatusError](https://aka.ms/AB-AA4e56x) - Could not communicate with the VM agent for snapshot status<br>
* [UserErrorRpCollectionLimitReached](https://aka.ms/AB-AA4e56l) - The Restore Point collection max limit has reached<br>
* [UserErrorKeyvaultPermissionNotConfigured](https://aka.ms/AB-AA4e56m) - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs<br>
* [ExtentionOperationFailed](https://aka.ms/AB-AA4e56c) - VMSnapshot extension operation failed<br>
* [BackUpOperationFailed/BackUpOperationFailedV2](https://aka.ms/AB-AA4ecqe) - Backup fails, with an internal error
