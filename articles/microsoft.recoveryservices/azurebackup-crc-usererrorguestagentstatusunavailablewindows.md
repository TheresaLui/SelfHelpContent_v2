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
## **VM agent unable to communicate with Azure Backup**
<!--/issueDescription-->

## **Recommended Steps**

We have identified that your backup operation might have failed, because our backup service could not communicate with the VM agent. To resolve this issue, follow the below steps:

1. Guest agent might be outdated, stopped or unresponsive. Follow [these](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms) instructions to update and restart the agent
2. [Ensure Backup extension running on the VM has outbound access to Azure public IP addresses](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#establish-network-connectivity)
3. Backup operation could fail if the backup extension is in an inconsistent state. To resolve this issue reinstall the extension by follow these [steps](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) and retry the operation.
