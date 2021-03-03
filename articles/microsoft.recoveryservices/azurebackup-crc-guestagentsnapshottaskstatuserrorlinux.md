<properties
	pageTitle="Guest Agent Snapshot Task Status Error: Linux"
	description="Guest Agent Snapshot Task Status Error: Linux"
	infoBubbleText="Could not communicate with the VM agent for snapshot status"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-guestagentsnapshottaskstatuserrorlinux"
	diagnosticScenario="azurebackup-crc-guestagentsnapshottaskstatuserrorlinux"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Guest Agent Snapshot Task Status Error: Linux

<!--issueDescription-->
Your backup operation might have failed because the backup service was unable to communicate with your VM's Guest Agent.
<!--/issueDescription-->

## **Recommended Steps**

1. Update the VM using the following PowerShell command: 

```
Select-AzSubscription -SubscriptionId <YourSubscription>
$vm = get-azvm -name <VMName> -resourcegroupname <RGName>
Update-AzVM -ResourceGroupName <RGName> -VM $vm*
```

2. [Update the Linux agent](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent) and retry the backup operation (you can try on-demand backup).

3. If the issue persists, use the following steps:
   - Check if the root drive has enough space
   - [Check Azure VM health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-1-check-azure-vm-health)
   - [Check Azure VM Guest Agent service health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health)
   - [Check Azure VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health)
   - [Check Azure Backup VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)

## **Recommended Documents**

* [Operating system support- Linux](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
