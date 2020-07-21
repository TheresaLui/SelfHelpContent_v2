<properties  
    pageTitle="I have an issue with my public IP"
    description="I have an issue with my public IP"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="scottAzure,timbasham"
    ms.author="scotro,tibasham"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615527"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6ce39c44-2a32-41c2-a8ce-7dedc93e6619"
	ownershipId="Compute_VirtualMachines_Content"
/>

# I have an issue with my public IP

4 out of 5 customers resolved their VM public IP issue using the steps below.

## **Recommended Documents**

Try using [Azure Bastion](data-blade:Microsoft_Azure_HybridNetworking.BastionHostBlade.resourceId.$resourceId) to connect to your VM.  [Azure Bastion](https://docs.microsoft.com/azure/bastion/bastion-overview) provides secure and seamless RDP connectivity to your virtual machine directly in the Azure portal over TLS. When you connect via Azure Bastion, your virtual machine does not need a public IP address, or inbound NSG rule allowing RDP traffic.

* [Guidelines on how to create, change or delete a public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address)
* [Guidelines on how to create, change or delete a public IP address prefix](https://docs.microsoft.com/azure/virtual-network/manage-public-ip-address-prefix)
* Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group or user defined route is blocking traffic to or from a virtual machine.
* [How to resolve an RDP failure due to NSG rules](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nsg-problem)

**Additional Documents**

* [Quick steps to address common RDP connection issues](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)
* [Follow the RDP troubleshooting guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)
* [Troubleshooting specific RDP error messages to a Windows VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-specific-rdp-errors)
