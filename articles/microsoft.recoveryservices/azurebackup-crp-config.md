<properties
	pageTitle="Azure IAAS VM Backup Configure Protection"
	description="Azure IAAS VM Backup Configure Protection failures"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32637322"
	resourceTags=""
	productPesIds="14749"
	articleId="8add52e9-c225-4d86-be81-e1175203382b"
	cloudEnvironments="public"
	/>

# Unable to Configure Backup for Azure Virtual Machines

## **Recommended Steps**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://aka.ms/AB-AA4ecq8) <br>
- [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress - Unable to initiate backup as another backup operation is currently in progress](https://aka.ms/AB-AA4e56y) <br>
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 4095GB](https://aka.ms/AB-AA4ecqf) <br>
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://aka.ms/AB-AA4ecqk) <br>
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://aka.ms/AB-AA4e56x) <br>
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://aka.ms/AB-AA4e56l) <br>
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://aka.ms/AB-AA4e56m) <br>
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://aka.ms/AB-AA4e56c) <br>
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://aka.ms/AB-AA4ecqe) <br>

## **Recommended Documents**

* [Azure Virtual Machine backup troubleshooting guide](https://aka.ms/AB-AA4ecqg)
