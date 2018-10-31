<properties
	pageTitle="Your virtual machine restarted due to an operating system fault"
	description="Your virtual machine restarted due to an operating system fault"
	infoBubbleText="Your virtual machine restarted due to an operating system fault"
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="dugill"
	articleId="servicehealthinsights-microsoft.classiccompute-virtualmachines-healthannotation_virtualmachinecrashed"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinecrashed"
/>

# Your virtual machine restarted due to an operating system fault

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable due to an operating system fault. Your virtual machine restarted and availability was restored at <!--$endTime--> endTime <!--/$endTime--> UTC. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed during this time.
<!--/issueDescription-->

To avoid data corruption operating system stops execution once it detects a serious error condition. Operating system might stop for many different reasons: a reference to a memory address that causes an access violation, an unexpected exception or trap, a faulting kernel mode driver and so on. Details about the cause of the error are written to the system log.

## Recommended steps
* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).

* **Learn about Windows bug check codes**: please refer to the following article: [bug check code reference](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/bug-check-code-reference2).