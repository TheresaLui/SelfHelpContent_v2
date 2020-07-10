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
## **Could not communicate with the VM agent for snapshot status**
<!--/issueDescription-->

## **Recommended Steps**
We have identified that your backup operation might have failed, because our backup service could not communicate with the VM agent. To resolve this issue, follow the below steps:

1. Guest agent might be outdated, stopped or unresponsive. Follow [these](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms) instructions to update and restart the agent.
2. [Ensure Backup extension running on the VM has outbound access to Azure public IP addresses](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#establish-network-connectivity)
3. Ensure there is enough free space in the **Root** drive
4. Ensure there are no pending OS updates


## **Recommended Documents**

* Learn more on [Operating system support- Linux](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
