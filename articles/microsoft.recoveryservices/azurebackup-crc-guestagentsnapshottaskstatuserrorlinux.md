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
We have identified that your backup operation might have failed, because the backup service was unable to communicate with your VM's Guest Agent.
<!--/issueDescription-->

## **Recommended Steps**

4 out of 5 customers resolved their backup failures by following these steps:
Step 1: **Update the VM using the following PowerShell command**<br> 
```
Select-AzSubscription -SubscriptionId <YourSubscription>
$vm = get-azvm -name <VMName> -resourcegroupname <RGName>
Update-AzVM -ResourceGroupName <RGName> -VM $vm*
```

Step 2: [Update the Linux agent](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent) and retry the backup operation (for ex. you can try on-demand backup).

If the issue persists, follow below steps:<br>
Step 3: Check if the root drive has enough space<br>
Step 4: [Check Azure VM health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-1-check-azure-vm-health)<br>
Step 5: [Check Azure VM Guest Agent service health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health)<br>
Step 6: [Check Azure VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health)<br>
Step 7: [Check Azure Backup VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)

## **Recommended Documents**

* Learn more on [Operating system support- Linux](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
