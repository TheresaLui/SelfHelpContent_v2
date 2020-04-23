<properties
	pageTitle="User Error Guest Agent Status Unavailable: Linux"
	description="User Error Guest Agent Status Unavailable: Linux"
	infoBubbleText="VM agent unable to communicate with Azure Backup"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorguestagentstatusunavailablelinux"
	diagnosticScenario="azurebackup-crc-usererrorguestagentstatusunavailablelinux"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# User Error Guest Agent Status Unavailable: Linux

<!--issueDescription-->
## VM agent unable to communicate with Azure Backup
<!--/issueDescription-->

## **Recommended Steps**
We have identified that your backup operation might have failed, because our backup service could not communicate with the VM agent. To resolve this issue, follow the below steps:

1. Guest agent might be outdated, stopped or unresponsive. Follow [these](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms) instructions to update and restart the agent.
2. [Ensure Backup extension running on the VM has outbound access to Azure public IP addresses](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#establish-network-connectivity)
3. Ensure there is enough free space in the **Root** drive
4. Ensure there are no pending OS updates


## **Recommended Documents**

* Learn more on [Operating system support - Linux](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
