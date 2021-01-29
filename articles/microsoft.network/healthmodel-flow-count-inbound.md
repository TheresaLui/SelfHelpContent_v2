<properties
pageTitle="High Inbound Connection/Flow Count"
description="High inbound connection/flow count may result in degraded performance."
infoBubbleText="Issues with VM network interface were detected. See details on the right."
service="microsoft.network"
resource="virtualmachines"
authors="dbrumley"
ms.author="dbrumley"
displayOrder=""
articleId="HealthModelFlowCountInbound"
diagnosticScenario="VmNetworkHealthInsights"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,Fairfax,Mooncake,Blackforest,usnat,ussec"
ownershipId="CloudNet_PhyNet"
/>

# We found an issue with the network interface on this VM
<!--issueDescription-->
Microsoft Azure has identified an issue with your VM, **<!--$vmname-->[vmname]<!--/$vmname-->**.  High inbound connection/flow count may result in degraded performance.
<!--/issueDescription-->

## **Recommended Steps**

The most likely cause of excessive flows is a customer vulnerability scanning tool that is performing port scanning for open or vulnerable ports on this VM.  If a scanning tool scans all destination ports on the network interface and uses a different source port for each connection, then high connection/flow count can result.
If you are running a vulnerability scanning tool, try disabling it for this VM.  If that resolves the problem, work with the vendor of the vulnerability scanning tool to reduce the number of different source ports used for inbound connections. 

If you are NOT running a vulnerability scanning tool, or disabling it does not resolve the problem, then try these additional steps:

* Login to the VM and display the source IP addresses of active connections (use command 'netstat -an' (Windows) or 'netstat -l' (Linux))
* If there are a large number of connections, examine the source IP (Foreign Address) to determine if they are legitimate or not

If the connections are legitimate then:

* Consider changing your application or service to reduce the number of connections on this network interface
* Consider enabling Accelerated Networking on the network interface
* Consider adding additional network interfaces to the VM to handle the connection volume
* Consider adding additional VMs to handle the connection volume
* Consider placing your VMs behind Azure Load Balancer to distribute connection volume

If the connections are NOT legitimate, in addition to above options, consider enabling Azure DDOS Protection Standard.


## **Recommended Documents**

* [Virtual machine network bandwidth](https://docs.microsoft.com/azure/virtual-network/virtual-machine-network-throughput)
* [Create a Windows VM with accelerated networking using Azure PowerShell](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
* [Create a Linux virtual machine with Accelerated Networking using Azure CLI](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli) 
* [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm)
* [Azure DDoS Protection Standard overview](https://docs.microsoft.com/azure/virtual-network/ddos-protection-overview)
* [What is Azure Load Balancer?](https://docs.microsoft.com/azure/load-balancer/load-balancer-overview)
* [Security groups](https://docs.microsoft.com/azure/virtual-network/security-overview)
* [Introduction to flow logging for network security groups](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-overview)
