<properties
	pageTitle="Your virtual machine was unavailable while it was being migrated to newer hardware"
	description="Your virtual machine was unavailable while it was being migrated to newer hardware"
	infoBubbleText="Your virtual machine was unavailable while it was being migrated to newer hardware"
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="dushyantgill"
	articleId="servicehealthinsights-microsoft.classiccompute-virtualmachines-healthannotation_virtualmachinemigrationinitiatedforplannedmaintenance"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinemigrationinitiatedforplannedmaintenance"
/>

# Your virtual machine was unavailable while it was being migrated to newer hardware

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable because it was migrated to newer hardware. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed.
<!--/issueDescription-->

Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. These updates range from patching software components in the hosting environment (like operating system, hypervisor, and various agents deployed on the host), to hardware decommissioning. The majority of these updates do not require a restart of the virtual machine. However, when maintenance requires a reboot of your virtual machine, you get a notice of when the maintenance is planned. In these cases, you'll also be given a time window where you can start the maintenance yourself, at a time that works for you.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents.

## Recommended steps

* **Learn more about about planned maintenance on Azure**: please read the following article: [planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/).

* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).

* **Learn when not to use virtual machine temporary disk**: data on the temporary disk is lost when the virtual machine is moved to a different host server. This may happen during maintenance events, or when you redeploy a VM. [Learn more about temporary disks](https://docs.microsoft.com/azure/virtual-machines/windows/about-disks-and-vhds#temporary-disk).