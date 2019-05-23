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
	cloudEnvironments="public"
/>

# Error UserErrorVmProvisioningStateFailed

<!--issueDescription-->
We identified that your backup operation failed due to the VM in failed provisioning state.
<!--/issueDescription-->

## **Recommended Steps**
To resolve UserErrorVmProvisioningStateFailed issue ensure that the VM is running or shut-down state for backup operation to succeed. If the VM requires a pending restart, then restart and retry the operation.<br/>

This error can occurs if any of one of the extension fails leaves the VM in a failed provisioned state. From portal, go to the extensions list, check if there is a failed extension. To troubleshoot and recover from [this](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics-vm-extension#troubleshoot-and-support) error refer to this document. If the VMSnapshot extension is in failed state, then follow [this](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) troubleshooting steps. If all extensions are in running state, check the health of the VM Agent by following troubleshooting steps for [Windows](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-but-unresponsive-for-windows-vms)/[Linux](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms).

