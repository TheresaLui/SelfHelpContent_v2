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
Could not communicate with the VM agent for snapshot status.
<!--/issueDescription-->

## **Recommended Steps**
- We have identified that your backup operation might have failed, because our backup service could not communicate with the VM agent. To resolve this issue, follow the steps listed in this [section](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health).
- Ensure [VM Extensions](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health) and [VM Backup Extension](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health) are healthy 
- Ensure there is enough free space in the **Root** drive
- Ensure there are no pending OS updates

## **Recommended Documents**

* Learn more on [Operating system support- Linux](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
