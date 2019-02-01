<properties
	pageTitle="configurationandsetup/unabletoreachaport"
	description="configurationandsetup/unabletoreachaport"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavinahar"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584255"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# configurationandsetup/unabletoreachaport

## **Recommended steps**

1. Check to ensure your application is listening on the specific port<br>
2. Ensure your NSG rule doesn't have a specific scource port mentioned, usually * is used
3. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade.id.$subscriptionId) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>

## **Recommended documents**

* [How to open porta to a virtual machine with the Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/nsg-quickstart-portal)<br>
* [Can't connect remotel to a VM because RDP port is not enabled in NSG](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nsg-problem)<br>
* [Troubleshoot SSH connections to an Azure Linux VM that fails, errors out, or is refused](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)<br>
* [Troubleshoot connections with Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal)<br>