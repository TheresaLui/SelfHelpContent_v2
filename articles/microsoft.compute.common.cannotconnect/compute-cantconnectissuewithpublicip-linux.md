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
    resourceTags="linux,redhat,Ubuntu"
    productPesIds="15571,15797,16454,16470,16342"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0b945377-40b3-4d60-90ef-5e37b98ad0af"
    ownershipId="Compute_VirtualMachines"
/>

# I have an issue with my public IP

4 out of 5 customers resolved their VM public IP issue using the steps below.

## **Recommended Documents**

Try using [Azure Bastion](https://docs.microsoft.com/azure/bastion/bastion-overview) to connect to your VM.  [Azure Bastion](https://docs.microsoft.com/azure/bastion/bastion-overview) provides secure and seamless RDP connectivity to your virtual machine directly in the Azure portal over TLS. When you connect via Azure Bastion, your virtual machine does not need a public IP address, or inbound NSG rule allowing RDP traffic.

* [Guidelines on how to create, change or delete a public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address)
* [Guidelines on how to create, change or delete a public IP address prefix](https://docs.microsoft.com/azure/virtual-network/manage-public-ip-address-prefix)
* Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group or user defined route is blocking traffic to or from a virtual machine

**Additional Documents**

* [Quick steps to diagnose & address common SSH connection issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)
* [Detailed SSH troubleshooting steps for issues connecting to a Linux VM in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)
* [Learn more about Network Security Groups](https://docs.microsoft.com/azure/virtual-network/security-overview)
* [How to reset local Linux password on Azure VMs](https://docs.microsoft.com/azure/virtual-machines/linux/reset-password)
* [How to use boot diagnostics to troubleshoot Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)

