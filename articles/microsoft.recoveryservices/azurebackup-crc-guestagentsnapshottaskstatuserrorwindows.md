<properties
      pageTitle="GuestAgentSnapshotTaskStatusErrorWindows"
      description="GuestAgentSnapshotTaskStatusErrorWindows"
      infoBubbleText="The Azure Backup service could not communicate with the VM Agent for triggering snapshot"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-guestagentsnapshottaskstatuserrorwindows"
      diagnosticScenario="azurebackup-crc-guestagentsnapshottaskstatuserrorwindows"
      selfHelpType="diagnostics"
      supportTopicIds="32553277"
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# GuestAgentSnapshotTaskStatusErrorWindows

<!--issueDescription-->
Your backup operation might have failed because the backup service was unable to communicate with your VM's Guest Agent.
<!--/issueDescription-->

## **Recommended Steps**

1. Update the VM by using the following PowerShell command:

```
Select-AzSubscription -SubscriptionId <YourSubscription>
$vm = get-azvm -name <VMName> -resourcegroupname <RGName>
Update-AzVM -ResourceGroupName <RGName> -VM $vm*
```
2. Retry the backup operation (you can try on-demand backup).

3. If the issue persists, follow below steps:
   - Check if the OS drive has enough space 
   - [Check Azure VM health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-1-check-azure-vm-health)
   - [Check Azure VM Guest Agent service health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health)
   - [Check Azure VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health)
   - [Check Azure Backup VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)
