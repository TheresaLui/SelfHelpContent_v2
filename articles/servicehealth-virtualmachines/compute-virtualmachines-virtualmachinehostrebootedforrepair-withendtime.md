<properties
	pageTitle="Your virtual machine wasn't available due to an unexpected failure on the host server"
	description="Your virtual machine wasn't available due to an unexpected failure on the host server"
	infoBubbleText="Your virtual machine wasn't available due to an unexpected failure on the host server"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="dushyantgill"
	articleId="servicehealthinsights-microsoft.compute-virtualmachines-healthannotation_virtualmachinehostrebootedforrepair-withendtime"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinehostrebootedforrepair-withendtime"
/>

# Your virtual machine wasn't available due to an unexpected failure on the host server

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable because of an unexpected failure on the server where it was hosted. The availability of your virtual machine was restored at <!--$endTime--> endTime <!--/$endTime--> UTC.
<!--/issueDescription-->

The reboot of the host server was triggered by Azure monitoring system that detected a potential failure condition with the host server. This caused your virtual machine to reboot as well. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed during this time.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents.

## Recommended steps

* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).