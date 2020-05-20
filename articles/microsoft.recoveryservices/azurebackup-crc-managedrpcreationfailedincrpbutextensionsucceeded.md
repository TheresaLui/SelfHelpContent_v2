<properties
    pageTitle="ManagedRPCreationFailedInCrpButExtensionSucceeded"
    description="ManagedRPCreationFailedInCrpButExtensionSucceeded"
    infoBubbleText="Backup operation failed for managed disk VM"
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-managedrpcreationfailedincrpbutextensionsucceeded"
    diagnosticScenario="azurebackup-crc-managedrpcreationfailedincrpbutextensionsucceeded"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>


# Error ManagedRPCreationFailedInCrpButExtensionSucceeded


<!--issueDescription-->
We have identified that the backup operation failed for the managed disk VM.
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, perform the below:

For Windows VM:

- Restart the Windows Guest Agent service and retry the backup operation
- [Ensure the Windows Guest Agent version is latest](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-but-unresponsive-for-windows-vms)
	
For Linux VM:

- Restart the Linux Guest Agent service and retry the backup operation
- [Ensure the Linux Guest Agent version is latest](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)
