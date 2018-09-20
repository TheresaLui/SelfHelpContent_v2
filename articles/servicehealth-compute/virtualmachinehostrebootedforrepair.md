<properties
	pageTitle="Your virtual machine isn't available because an unexpected failure on the host server"
	description="Virtual Machine Host Rebooted For Repair"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_virtualmachinehostrebootedforrepair"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinehostrebootedforrepair"
/>

# Your virtual machine isn't available because an unexpected failure on the host server

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> and availability was restored at <!--$endTime--> EndTime <!--/$endTime--> (UTC).
This unexpected occurrence was caused by an unexpected failure on the host server.

The host node reboot was triggered by our Azure monitoring systems detecting a potential failure condition with the physical node where the virtual machine was hosted. This caused your VM to get rebooted as well. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. 

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.  
To learn more about high availability options, please refer to the following articles:

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)

* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents of Virtual Machines.