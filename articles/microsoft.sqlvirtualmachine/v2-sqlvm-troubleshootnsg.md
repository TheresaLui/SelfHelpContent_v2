<properties
	pageTitle="Troubleshoot network security group (NSG)"
	description="Troubleshoot network security group (NSG)"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740107"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="35bf8dd8-d553-42c6-b4db-3bc683e007cc"
	ownershipId="AzureData_AzureSQLVM"
/>



# Troubleshoot my Network Security Group (NSG)

4 out of 5 customers resolved their VM Network Security Group issue using the steps below.<br>

## **Recommended Steps**

NSGs by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps.<br>

1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group is blocking traffic to or from a virtual machine
2. Edit the [Network Security Group](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group) to make changes to the rules if needed
3. If there is no rule to allow the traffic from Internet, add a new rule to allow access to the backend port, with source being 'Internet', '\*' or a specific public IP address

## **Recommended Documents**

* [Network Security Groups (NSGs) Overview](https://docs.microsoft.com/azure/virtual-network/security-overview)<br>
* [How to troubleshoot Network Security Groups (NSGs)](https://docs.microsoft.com/azure/virtual-network/diagnose-network-traffic-filter-problem)<br>
* [How to configure Network Watcher to troubleshoot NSG issues](https://docs.microsoft.com/azure/network-watcher/network-watcher-create)<br>
* [How to configure NSG logs in the Azure portal](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal)<br>
* [How to read NSG logs generated from Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)<br>
* [Filter network traffic with a network security group using the Azure Portal](https://docs.microsoft.com/azure/virtual-network/tutorial-filter-network-traffic)
