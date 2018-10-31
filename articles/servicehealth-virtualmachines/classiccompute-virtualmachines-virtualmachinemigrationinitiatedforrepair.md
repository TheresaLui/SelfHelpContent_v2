<properties
	pageTitle="Your virtual machine was unavailable while it was being migrated to another host server"
	description="Your virtual machine was unavailable while it was being migrated to another host server"
	infoBubbleText="Your virtual machine was unavailable while it was being migrated to another host server"
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="dugill"
	articleId="servicehealthinsights-microsoft.classiccompute-virtualmachines-healthannotation_virtualmachinemigrationinitiatedforrepair"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinemigrationinitiatedforrepair"
/>

# Your virtual machine was unavailable while it was being migrated to another host server

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable because of an unexpected failure on the server where it was hosted. Your virtual machine was automatically moved to another host server and availability was restored at <!--$endTime--> endTime <!--/$endTime--> UTC.
<!--/issueDescription-->

The reboot of the host server was triggered by Azure monitoring system that detected a potential failure condition with the host server. As a result, your virtual machine was automatically moved to a different and healthy host server to avoid further impact. This caused your virtual machine to reboot. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed during this time.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents.

## Recommended steps

* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).

* **Learn when not to use virtual machine temporary disk**: data on the temporary disk is lost when the virtual machine is moved to a different host server. This may happen during maintenance events, or when you redeploy a VM. [Learn more about temporary disks](https://docs.microsoft.com/azure/virtual-machines/windows/about-disks-and-vhds#temporary-disk).  

* **Learn more about automated recovery action**: please read the following article: [auto-recovery of virtual machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines).
