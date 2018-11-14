<properties
	pageTitle="ExtensionSnapshotFailedNoNetwork"
	description="ExtensionSnapshotFailedNoNetwork"
	infoBubbleText="Backup operation failed due to network connectivity issues. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	articleId="azurebackup-crc-extensionsnapshotfailednonetwork"
	diagnosticScenario="azurebackup-crc-extensionsnapshotfailednonetwork"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ExtensionSnapshotFailedNoNetwork
<!--issueDescription-->
Backup operation failed due to network connectivity issues or restricted access to your Azure storage account.
<!--/issueDescription-->

## **Recommended Steps**
We identified that your backup operation failed because the snapshot isn't triggered due to network connectivity issue with the Azure storage account. Complete the troubleshooting steps mentioned below and then retry your operation.

1. From virtual machine, launch browser and check if you are able to access any public facing Internet site. If not, then there is restrictions on making outbound calls from the VM.
2. From virtual machine properties **Settings** > **Networking** > **Outbound Port Rule** check if there are NSG rules with DENY action. Follow this [step-by-step video](https://www.youtube.com/watch?v=1EjLQtbKm1M) to use Service Tags to [enable access to storage endpoints](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#create-a-path-for-https-traffic).
3. If you are using a HTTP Proxy server to have restrict output bound traffic, then follow these steps to [enable access to storage endpoints](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#create-a-path-for-https-traffic).
4. Ensure guest agent is installed and responsive in the VM by following these steps for the [Windows VM](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-but-unresponsive-for-windows-vms) or [Linux](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms).
5. DHCP must be enabled inside the guest for the IaaS VM backup to work.
