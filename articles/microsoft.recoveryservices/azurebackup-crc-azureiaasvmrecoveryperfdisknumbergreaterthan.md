<properties
	pageTitle="AzureIaaSVMRecoveryPerfDiskNumberGreaterThan8"
	description="AzureIaaSVMRecoveryPerfDiskNumberGreaterThan8"
	infoBubbleText="the restore operation is taking long time to complete because the number of disks attached to the VM is greater than eight"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-azureiaasvmrecoveryperfdisknumbergreaterthan8"
	diagnosticScenario="azurebackup-crc-azureiaasvmrecoveryperfdisknumbergreaterthan8"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error AzureIaaSVMRecoveryPerfDiskNumberGreaterThan8

<!--issueDescription-->
We have identified that the restore operation is taking a long time to complete because the number of disks attached to the VM is greater than eight disks.
<!--/issueDescription-->

## **Recommended Steps**

Restore performance can also be impacted by the following factors:

- If you are trying to restore from vault, we highly recommend that you select a storage account that isn't loaded with other application writes and reads
- Try to modify the scheduled time for the VM to reduce the queue time, in case of restore traffic
- Use instant restore (recovery type is snapshot) where available, to reduce the restore time 
- If you are using PowerShell to restore from a snapshot, then use or add the `TargetResourceGroupName` parameter in your Automation Runbook. For more information, see this [Restore managed disks](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-managed-disks)
