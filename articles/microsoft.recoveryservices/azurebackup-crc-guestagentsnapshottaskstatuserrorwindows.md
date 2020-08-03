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
Could not communicate with the VM agent for snapshot status
<!--/issueDescription-->

## **Recommended Steps**

- We have identified that your backup operation might have failed, because our backup service could not communicate with the VM agent. To resolve this issue, follow the steps listed in this [section](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health)
- - Ensure [VM Extensions](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health) and [VM Backup Extension](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health) are healthy
