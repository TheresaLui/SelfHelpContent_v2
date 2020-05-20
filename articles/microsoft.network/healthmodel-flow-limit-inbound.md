<properties
pageTitle="Inbound Flow Limit Exceeded"
description="VM network interface is dropping some inbound connections due to the number of flows exceeding the 500K flow limit"
infoBubbleText="Issues with VM network interface were detected. See details on the right."
service="microsoft.network"
resource="virtualmachines"
authors="dbrumley"
ms.author="dbrumley"
displayOrder=""
articleId="HealthModelFlowLimitInbound"
diagnosticScenario="VmNetworkHealthInsights"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,Fairfax,Mooncake,Blackforest, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# We found an issue with the network interface on this VM
<!--issueDescription-->
Microsoft Azure has identified an issue with your VM, **<!--$vmname-->[vmname]<!--/$vmname-->**.  Some inbound connections are being dropped due to 500K flow limit exceeded on the network interface.
<!--/issueDescription-->

## **Recommended Steps**

The most likely cause of excessive flows is a customer vulnerability scanning tool that is performing port scanning for open or vulnerable ports on this VM.  If a scanning tool scans all destination ports on the network interface and uses a different source port for each connection, then the total number of flows could exceed the 500K limit.
If you are running a vulnerability scanning tool, try disabling it for this VM.  If that resolves the problem, work with the vendor of the vulnerability scanning tool to reduce the number of different source ports used for inbound connections. 

If you are NOT running a vulnerability scanning tool, or disabling it does not resolve the problem, then try these additional steps:

* Login to the VM and display the source IP addresses of active connections (use command 'netstat -an' (Windows) or 'netstat -l' (Linux)).
* If there are a large number of connections, examine the source IP (Foreign Address) to determine if they are legitimate or not.
* If the connections are legitimate, change your application to reduce the number of connections on this network interface, or add additional network interfaces to the VM.
* If the connections are not legitimate, consider enabling Azure DDOS Protection Standard or placing the VM behind Azure Load Balancer.<br><br>

If you do NOT see a large number of connections within the VM with 'netstat' command, then the connections are possibly being blocked by Network Security Group rule, but still contributing to the 500K flow limit.  Try enabling flow logging for network security groups and determine from the flow logs whether the connections are legitimate or not.  

* If the connections are legitimate, change your application to reduce the number of connections on this network interface, or add additional network interfaces to the VM.
* If the connections are not legitimate, consider enabling Azure DDOS Protection Standard or placing the VM behind Azure Load Balancer.



## **Recommended Documents**

* [Virtual machine network bandwidth](https://docs.microsoft.com/azure/virtual-network/virtual-machine-network-throughput)
* [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm)
* [Azure DDoS Protection Standard overview](https://docs.microsoft.com/azure/virtual-network/ddos-protection-overview)
* [What is Azure Load Balancer?](https://docs.microsoft.com/azure/load-balancer/load-balancer-overview)
* [Security groups](https://docs.microsoft.com/azure/virtual-network/security-overview)
* [Introduction to flow logging for network security groups](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-overview)
