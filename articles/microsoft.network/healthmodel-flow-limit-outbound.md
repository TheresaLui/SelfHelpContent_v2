<properties
pageTitle="Outbound Flow Limit Exceeded"
description="VM network interface is dropping some outbound connections due to the number of flows exceeding the flow limit"
infoBubbleText="Issues with VM network interface were detected. See details on the right."
service="microsoft.network"
resource="virtualmachines"
authors="dbrumley"
ms.author="dbrumley"
displayOrder=""
articleId="HealthModelFlowLimitOutbound"
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
Microsoft Azure has identified an issue with your VM, **<!--$vmname-->[vmname]<!--/$vmname-->**.  Some outbound connections are being dropped due to flow limit exceeded on the network interface.
<!--/issueDescription-->

## **Recommended Steps**

The most likely cause of excessive outbound connections/flows is a customer application or service within the VM.   

* Login to the VM and display the destination IP addresses of active connections (use command 'netstat -an' (Windows) or 'netstat -l' (Linux))
* Configure your application or service to reduce the number of outbound connections or add additional network interfaces to the VM or add additional VMs

## **Recommended Documents**

* [Virtual machine network bandwidth](https://docs.microsoft.com/azure/virtual-network/virtual-machine-network-throughput)
* [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm)
