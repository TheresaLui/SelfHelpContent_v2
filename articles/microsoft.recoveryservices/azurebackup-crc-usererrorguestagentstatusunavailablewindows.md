<properties
	pageTitle="User Error Guest Agent Status Unavailable: Windows"
	description="User Error Guest Agent Status Unavailable: Windows"
	infoBubbleText="VM agent unable to communicate with Azure Backup"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	articleId="azurebackup-crc-usererrorguestagentstatusunavailablewindows"
	diagnosticScenario="azurebackup-crc-usererrorguestagentstatusunavailablewindows"
	selfHelpType="diagnostics"
	supportTopicIds="32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
  	ownershipId="StorageMediaEdge_Backup"
/>

# User Error Guest Agent Status Unavailable: Windows

<!--issueDescription-->
Your backup operation might have failed because the backup service was unable to communicate with your VM's Guest Agent.
<!--/issueDescription-->

## **Recommended Steps**

1. Update the VM by using the following PowerShell command:

```
Select-AzSubscription -SubscriptionId <YourSubscriptionID>
$vm = get-azvm -name <VMName> -resourcegroupname <RGName>
Update-AzVM -ResourceGroupName <RGName> -VM $vm*
```

2. Retry the backup operation (you can try on-demand backup).

3. If the issue persists, use the following steps:
   - Check if the OS drive has enough space 
   - [Check Azure VM health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-1-check-azure-vm-health)
   - [Check Azure VM Guest Agent service health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health)
   - [Check Azure VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health)
   - [Check Azure Backup VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)
