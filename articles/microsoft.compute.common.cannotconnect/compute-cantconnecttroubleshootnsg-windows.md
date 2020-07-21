<properties  
    pageTitle="Troubleshoot my Network Security Group (NSG)"
    description="Troubleshoot my Network Security Group (NSG)"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="scottAzure,timbasham"
    ms.author="scotro,tibasham"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615533,32639647"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c5ccfcb5-7f2c-47d9-bc8b-46b6beab5480"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshoot my Network Security Group (NSG)

4 out of 5 customers resolved their VM Network Security Group issue using the steps below.<br>

## **Recommended Steps**

NSGs by default deny connections from the Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps:

Try using [Azure Bastion](data-blade:Microsoft_Azure_HybridNetworking.BastionHostBlade.resourceId.$resourceId) to connect to your VM.  [Azure Bastion](https://docs.microsoft.com/azure/bastion/bastion-overview) provides secure and seamless RDP connectivity to your virtual machine directly in the Azure portal over TLS. When you connect via Azure Bastion, your virtual machine does not need a public IP address, or inbound NSG rule allowing RDP traffic.

1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group is blocking traffic to or from a virtual machine
2. Edit the [Network Security Group](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group) to make changes to the rules if needed.
3. If there is no rule to allow remote RDP traffic, review [Unable to connect via RDP due to NSG](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nsg-problem)<br>
4. If there is no rule to allow the traffic from Internet, add a new rule to allow access to the backend port, with source being 'Internet', '\*' or a specific public IP address

## **Recommended Documents**

* [How to troubleshoot Network Security Groups (NSGs)](https://blogs.msdn.microsoft.com/mvpawardprogram/2018/05/08/troubleshoot-nsgs)<br>
* [How to configure Network Watcher to troubleshoot NSG issues](https://docs.microsoft.com/azure/network-watcher/network-watcher-create)<br>
* [How to read NSG logs generated from Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)<br>
* [Filter network traffic with a network security group using the Azure Portal](https://docs.microsoft.com/azure/virtual-network/tutorial-filter-network-traffic)
