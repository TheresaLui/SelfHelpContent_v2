<properties
	pageTitle="extensionstuckindeletionstate"
	description="extensionstuckindeletionstate"
	infoBubbleText="Extension state is not supportive to backup operation."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	articleId="azurebackup-crc-extensionstuckindeletionstate"
	diagnosticScenario="azurebackup-crc-extensionstuckindeletionstate"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# ExtensionStuckInDeletionState

<!--issueDescription-->
## **Extension state is not supportive to backup operation.**
<!--/issueDescription-->

## **Recommended Steps**
We have identified your backup operation failed due to inconsistent state of Backup Extension.

To resolve this issue, follow these steps:

* Ensure Guest Agent is installed and responsive
* From Azure portal go to **Virtual Machine** > **All Settings** > **Extensions**
* Select the backup extension VmSnapshot or VmSnapshotLinux and click **Uninstall**
* After deleting backup extension retry the backup operation
* The subsequent backup operation will install the new extension in the desired state


## **Recommended Documents**

* Troubleshoot backup issues in [Windows VM](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-but-unresponsive-for-windows-vms)
* Troubleshoot backup issues in [Linux VM](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)
