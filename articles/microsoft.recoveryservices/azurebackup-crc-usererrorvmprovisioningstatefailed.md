<properties
	pageTitle="UserErrorVmProvisioningStateFailed"
	description="UserErrorVmProvisioningStateFailed"
	infoBubbleText="VM is in Failed Provisioning State"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorvmprovisioningstatefailed"
	diagnosticScenario="azurebackup-crc-usererrorvmprovisioningstatefailed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorVmProvisioningStateFailed

<!--issueDescription-->
We identified that your backup operation failed due to the VM being in a failed provisioning state. This error can occur if any of one of the extensions fail, leaving the VM in a failed provisioned state. To resolve the "UserErrorVmProvisioningStateFailed" issue, ensure that the VM is running or in a shut-down state for the backup operation to succeed. If the VM requires a pending restart, restart and retry the operation.
<!--/issueDescription-->

## **Recommended Steps**

* From the Azure portal, go to the extensions list and check if there is a failed extension
* Attempt to [troubleshoot and recover](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics-vm-extension#troubleshoot-and-support) from the error
* If the VMSnapshot extension is in **failed** state, follow [these](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) troubleshooting steps
* If all extensions are running, check the health of the VM Agent by following troubleshooting steps for [Windows](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-but-unresponsive-for-windows-vms) or [Linux](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)


