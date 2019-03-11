<properties
	pageTitle="Your virtual machine wasn't available because it lost connectivity to its remote disk"
	description="Your virtual machine wasn't available because it lost connectivity to its remote disk"
	infoBubbleText="Your virtual machine wasn't available because it lost connectivity to its remote disk"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="dushyantgill"
	articleId="servicehealthinsights-microsoft.compute-virtualmachines-healthannotation_virtualmachinestorageoffline"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinestorageoffline"
/>

# Your virtual machine wasn't available because it lost connectivity to its remote disk

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable because it lost connectivity to its remote disk.
<!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your virtual machine to Azure Storage service where your virtual machine's disks reside. If transactions do not complete successfully within 120 seconds (inclusive of retries), connectivity is considered to be lost and your virtual machine is shut down temporarily. This is done to preserve data integrity and prevent corruption of your virtual machine. Once Azure platform detects that connectivity to Storage service is restored, your virtual machine is automatically restarted. RDP and SSH connections to your virtual machine, or requests to any services running inside your virtual machine may have failed during this time.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents.

## Recommended steps

* **Configure your virtual machines for high availability**: the best way to protect an application against virtual machine reboots and downtime is to [configure your virtual machines for high availability](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability). We recommend that you group two or more virtual machines in an Availability Set. This configuration ensures that during either a planned or unplanned maintenance event, at least one virtual machine is available and meets the 99.95 percent [Azure SLA](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_5/).

* **Use Managed Disks with Availability Sets**: Managed Disks provides better reliability for Availability Sets by ensuring that the disks of VMs in an Availability Set are sufficiently isolated from each other to avoid single points of failure. [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)