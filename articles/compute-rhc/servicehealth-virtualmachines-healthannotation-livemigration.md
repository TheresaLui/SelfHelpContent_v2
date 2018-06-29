<properties
	pageTitle="Your virtual machine was paused for a memory-preserving update"
	description=""
	infoBubbleText="Your virtual machine was paused. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="dushyantgill"
	displayOrder=""
	articleId="ServiceHealth-VirtualMachines-HealthAnnotation-LiveMigration"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Your virtual machine was paused for a memory-preserving update

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime-->, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> was paused for a memory-preserving update.
<!--/issueDescription-->

Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. These updates range from patching software components in the hosting environment (like operating system, hypervisor, and various agents deployed on the host), upgrading networking components, to hardware decommissioning. The majority of these updates do not require a restart of the virtual machine. Instead, they are applied by simply pausing the virtual machines for a few seconds.

These memory-preserving updates are accomplished with technology that enables in-place live migration. When it is being updated, the VM is placed in a paused state. This state preserves the memory in RAM while the underlying host operating system receives the necessary updates and patches. The VM is resumed within 30 seconds of being paused. After the VM is resumed, its clock is automatically synchronized. Multi-instance updates (for VMs in an availability set) are applied one update domain at a time.

## **Recommended steps**

* **Configure your VMs for high availability**: the best way to protect an application that's running on Azure against virtual machine reboots and downtime is to configure the them for high availability. We recommend that you group two or more virtual machines in an availability set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).
