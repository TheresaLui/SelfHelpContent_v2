<properties
	pageTitle="Diagnose and resolve issues with Windows Azure virtual machine backup"
	description="Diagnose and resolve issues with Windows Azure virtual machine backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
	articleId="79088548-2aa6-44f1-8f3c-25df1e8e92bf"
/>

# Diagnose and resolve issues with Windows Azure virtual machine backup

## **Recommended Steps**

- [Ensure your Windows VM agent is up to date before troubleshooting further](https://aka.ms/AB-AA4ecqu) <br>
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://aka.ms/AB-AA4ecqj) <br>
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://aka.ms/AB-AA4e56b) <br>
- [OS Versions older than Windows Server 2008 R2 are not supported for Backup](https://aka.ms/AA4evhu)

## **Recommended Documents**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://aka.ms/AB-AA4ecq8) <br>
- [UserErrorStandardSSDNotSupported - Currently Azure Backup does not support Standard SSD disks](https://aka.ms/AB-AA4ecqd) <br>
- [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress - Unable to initiate backup as another backup operation is currently in progress](https://aka.ms/AB-AA4e56y) <br>
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 1023GB](https://aka.ms/AB-AA4ecqf) <br>
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://aka.ms/AB-AA4ecqk) <br>
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://aka.ms/AB-AA4e56x) <br>
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://aka.ms/AB-AA4e56l) <br>
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://aka.ms/AB-AA4e56m) <br>
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://aka.ms/AB-AA4e56c) <br>
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://aka.ms/AB-AA4ecqe) <br>
