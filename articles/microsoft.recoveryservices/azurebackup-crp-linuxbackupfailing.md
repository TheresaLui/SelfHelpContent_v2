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
	resourceTags="linux"
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public"
	articleId="f82b1ed9-9c4b-4061-93af-3e54d91e3426"
/>

# Azure Backup - Backup is failing for my VM

## **Recommended Steps**
- [Ensure your Linux VM agent is up to date before troubleshooting further](https://aka.ms/AB-AA4ecq9)<br>
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://aka.ms/AB-AA4ecqy)<br>
- [If your Linux OS/Kernel version is not listed here, then it is not supported](https://aka.ms/AB-AA4ecr1)<br>
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://aka.ms/AB-AA4ecq1)<br>
- [If your issue is still not resolved, check VM Backup troubleshooting guide](https://aka.ms/AB-AA4ecq1)<br>

## **Recommended Documents**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://aka.ms/AB-AA4ecq8) <br>
- [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress - Unable to initiate backup as another backup operation is currently in progress](https://aka.ms/AB-AA4e56y) <br>
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 4095GB](https://aka.ms/AB-AA4ecqf) <br>
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://aka.ms/AB-AA4ecqk) <br>
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://aka.ms/AB-AA4e56x) <br>
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://aka.ms/AB-AA4e56l) <br>
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://aka.ms/AB-AA4e56m) <br>
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://aka.ms/AB-AA4e56c) <br>
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://aka.ms/AB-AA4ecqe) <br>
