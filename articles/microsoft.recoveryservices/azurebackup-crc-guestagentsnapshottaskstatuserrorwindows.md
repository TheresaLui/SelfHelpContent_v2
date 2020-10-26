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
We have identified that your backup operation might have failed, because the backup service was unable to communicate with your VM's Guest Agent.
<!--/issueDescription-->

## **Recommended Steps**

4 out of 5 customers resolved their backup failures by following these steps:

Step 1: **Update the VM using the following PowerShell command**<br> 
*Select-AzSubscription -SubscriptionId “YourSubscriptionID” $vm = get-azvm -name VMName -resourcegroupname RGName Update-AzVM -ResourceGroupName RGName VM $vm* <br>

Retry the backup operation (for ex. you can try on-demand backup). If the issue persists, follow below steps:

Step 2: Check if the OS drive has enough space <br>
Step 3: [Check Azure VM health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-1-check-azure-vm-health)<br>
Step 4: [Check Azure VM Guest Agent service health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health)<br>
Step 5: [Check Azure VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health)<br>
Step 6: [Check Azure Backup VM extension health](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)
