<properties
	pageTitle="Your virtual machine was unavailable due to an Azure issue"
	description="Your virtual machine was unavailable due to an Azure issue"
	infoBubbleText="Your virtual machine was unavailable due to an Azure issue"
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="dushyantgill"
	articleId="servicehealthinsights-microsoft.classiccompute-virtualmachines-healthannotation_no_reason"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_no_reason"
/>

# Your virtual machine was unavailable due to an Azure issue

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable due to an Azure issue. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed.
<!--/issueDescription-->

Unexpected events in the Azure platfom can cause your virtual machine to reboot. These include [host server faults](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#host-server-faults), [auto-recovery](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines/), [unplanned maintenance](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#unplanned-maintenance), [virtual machine crashes](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#vm-crashes), and [storage-related forced shutdowns](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#storage-related-forced-shutdowns). In rare circumstances, a widespread service issue can affect many Azure virtual machines. For such widespread service issues, Azure team notifies affected customers via [Azure Service Health](https://portal.azure.com/#blade/Microsoft_Azure_Health/AzureHealthBrowseBlade/serviceIssues). 

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents.

## Recommended steps

* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).

* **View Azure Service Health**: please view the platform health of your Azure services in [Azure Service Health](https://portal.azure.com/#blade/Microsoft_Azure_Health/AzureHealthBrowseBlade/serviceIssues).  