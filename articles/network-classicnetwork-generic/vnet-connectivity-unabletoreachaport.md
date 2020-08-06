<properties
	pageTitle="configurationandsetup/unabletoreachaport"
	description="configurationandsetup/unabletoreachaport"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavinahar"
	ms.author="anavin"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584255"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="867463"
	ownershipId="CloudNet_VirtualNetwork"
/>

# configurationandsetup/unabletoreachaport

## **Recommended Steps**

1. Check to ensure your application is listening on the specific port. There are multiple ways to do this, [netstat](https://docs.microsoft.com/windows-server/administration/windows-commands/netstat) is an example<br>
2. Ensure your NSG rule doesn't have a specific [source port mentioned (usually *)](https://docs.microsoft.com/azure/virtual-network/security-overview#security-rules)<br>
3. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade.id.$subscriptionId) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>

## **Recommended Documents**

* [How to open ports to a virtual machine with the Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/nsg-quickstart-portal)<br>
* [Can't connect remotely to a VM because RDP port is not enabled in NSG](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nsg-problem)<br>
* [Troubleshoot SSH connections to an Azure Linux VM that fails, errors out, or is refused](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)<br>
* [Troubleshoot connections with Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal)<br>
