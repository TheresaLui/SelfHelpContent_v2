<properties
	pageTitle="Your virtual machine was paused for a memory-preserving update"
	description="Your virtual machine was paused for a memory-preserving update"
	infoBubbleText="Your virtual machine was paused for a memory-preserving update"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="dushyantgill"
	articleId="servicehealthinsights-microsoft.compute-virtualmachines-healthannotation_livemigrationcompleted"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_livemigrationcompleted"
/>

# Your virtual machine was paused for a memory-preserving update

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> was paused for a memory-preserving update. This caused your virtual machine to be unavailable for a few seconds. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed during this time.
<!--/issueDescription-->

Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. These updates range from patching software components in the hosting environment (like operating system, hypervisor, and various agents deployed on the host), to hardware decommissioning. The majority of these updates do not require a restart of the virtual machine. Instead, they are applied by simply pausing the virtual machines for a few seconds. These memory-preserving updates are accomplished with technology that enables in-place live migration. During the update, the virtual machine is placed in a paused state. This state preserves the memory in RAM while the underlying host operating system receives the necessary updates. The virtual machine is resumed within 30 seconds of being paused. After the virtual machine is resumed, its clock is automatically synchronized. 

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents.

## Recommended steps

* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).

* **Learn more about memory-preserving operations**: please refer to the following article: [planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/).