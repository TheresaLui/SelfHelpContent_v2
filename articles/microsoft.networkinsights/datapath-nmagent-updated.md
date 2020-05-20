<properties
pageTitle="Physical host node underwent regular maintenance update recently"
description="The physical host node where was undergoing a regular maintenance of the networking stack. This impacted connectivity briefly."
infoBubbleText="Networking stack maintenance. See details on the right"
service="microsoft.compute"
resource="virtualmachines"
authors="rkrir"
ms.author="krisragh"
displayOrder="17"
articleId="NmAgentUpdated"
diagnosticScenario="NmAgentUpdated"
selfHelpType="resource"
supportTopicIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>

If you have verified that the customer's impact is primarily due to NMAgent update, please adapt the root cause statement below:

# We ran diagnostics on your VM and found an issue

The physical host node where your VM was running was undergoing a regular maintenance of the networking stack. This impacted connectivity briefly.

Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. The purpose of these updates ranges from patching software components in the hosting environment to upgrading networking components or decommissioning hardware. Updates rarely affect hosted VMs. When updates do have an effect, Azure chooses the least impactful method for updates, which may sometimes still result in a brief downtime or connectivity loss. We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you.

## **Recommended Steps**

To prepare for VM maintenance and reduce its impact, try using Scheduled Events for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) or [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events). Azure also provides full control over such platform maintenance on [Azure Dedicated Hosts](https://docs.microsoft.com/azure/virtual-machines/windows/dedicated-hosts) and [Isolated VMs](https://docs.microsoft.com/azure/security/fundamentals/isolation-choices). For general information, please refer to [Maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)
