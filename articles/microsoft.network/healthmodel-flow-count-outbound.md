<properties
pageTitle="High Outbound Connection/Flow Count"
description="High outbound connection/flow count may result in degraded performance."
infoBubbleText="Issues with VM network interface were detected. See details on the right."
service="microsoft.network"
resource="virtualmachines"
authors="dbrumley"
ms.author="dbrumley"
displayOrder=""
articleId="HealthModelFlowCountOutbound"
diagnosticScenario="VmNetworkHealthInsights"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,Fairfax,Mooncake,Blackforest,USNat,USSec"
ownershipId="CloudNet_PhyNet"
/>

# We found an issue with the network interface on this VM
<!--issueDescription-->
Microsoft Azure has identified an issue with your VM, **<!--$vmname-->[vmname]<!--/$vmname-->**.  High outbound connection/flow count may result in degraded performance.
<!--/issueDescription-->

## **Recommended Steps**

The most likely cause of high outbound connections/flows is a customer application or service within the VM.   

* Consider changing your application or service to reduce the number of connections on this network interface
* Consider enabling Accelerated Networking on the network interface
* Consider adding additional network interfaces to the VM to handle the connection volume
* Consider adding additional VMs to handle the connection volume

To determine the nature of the traffic, log in to the VM and display the destination IP addresses of active connections: use command **netstat -an** on Windows, or command **netstat -l** on Linux.


## **Recommended Documents**

* [Virtual machine network bandwidth](https://docs.microsoft.com/azure/virtual-network/virtual-machine-network-throughput)
* [Create a Windows VM with accelerated networking using Azure PowerShell](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
* [Create a Linux virtual machine with Accelerated Networking using Azure CLI](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli) 
* [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm)
