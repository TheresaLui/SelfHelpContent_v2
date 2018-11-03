<properties
	pageTitle: "extensionsnapshotfailednonetwork"
	description: "ExtensionSnapshotFailedNoNetwork"
	service: "microsoft.recoveryservices"
	infoBubbleText: "Backup operation failed due to network connectivity issues or restricted access to your Azure storage account."
	service: "microsoft.recoveryservices"
	resource: "backup"
	authors: "srinathv"
	articleId: "azurebackup-crc-extensionsnapshotfailednonetwork"
		selfHelpType: "diagnostics"
	supportTopicIds: "32553276,32553277,32553285"
	productPesIds: "15207"
	cloudEnvironments: "public"
/>

# ExtensionSnapshotFailedNoNetwork
<!--issueDescription-->
## Backup operation failed due to network connectivity issues or restricted access to your Azure storage account.
<!--/issueDescription-->

We identified that your backup operation failed because the snapshot isn't triggered. Complete the troubleshooting steps mentioned below and then retry your backup operation.

## **Recommended Steps**
1. From Virtual Machine, launch browser and check if you are able to access any public facing Internet site. If not, then there is restrictions on making outbound calls from the VM.
2. From virtual machine properties Settings > Networking > Outbound Port Rule check if there are NSG rules with DENY action. Follow this [step-by-step video](https://www.youtube.com/watch?v=1EjLQtbKm1M) to use Service Tags to enable access to storage endpoints (Azure Public IP addresses).
3. If you are using a HTTP Proxy server to have restrict output bound traffic, then follow these steps to enable access to storage endpoints (Azure Public IP addresses).
4. Ensure guest agent is installed and responsive by following these steps for Windows VM or Linux VM.
5. DHCP must be enabled inside the guest for the IaaS VM backup to work.
