<properties
pageTitle="Physical host node underwent regular maintenance update recently"
description="The physical host node where was undergoing a regular maintenance of the networking stack. This impacted connectivity briefly."
infoBubbleText="Networking stack maintanence. See details on the right"
service="microsoft.compute"
resource="virtualmachines"
authors="rkrir"
ms.author="krisragh"
displayOrder="17"
articleId="NmAgentUpdated"
diagnosticScenario="NmAgentUpdated"
selfHelpType="resource"
supportTopicIds=""
cloudEnvironments="Public"
/>

# We ran diagnostics on your VM and found an issue

Microsoft Azure team has finished investigating the issue with your virtual machine. The physical host node where your VM was running was undergoing a regular maintenance of the networking stack. This impacted connectivity briefly.    

Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. There is an expected downtime during these updates. We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you. 

## **Recommended Steps**

If the VM experienced downtime or connectivity loss during this update, it is to be expected. There is guidance (for [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) and [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events)) on how to prepare and design for such maintenance.

Note that [virtual functions are expected to be revoked during servicing updates](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli?toc=%2Fazure%2Fvirtual-machines%2Flinux%2Ftoc.json#handle-dynamic-binding-and-revocation-of-virtual-function).

[Azure Dedicated Host](https://azure.microsoft.com/blog/introducing-azure-dedicated-host/) may be an option to consider if you would like more stringent control over the updates in the future.
