<properties
	pageTitle="Host OS RCA"
	description="Platform Operation - Maintenance"
	infoBubbleText="Found maintenance events. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="zjalexander"
	ms.author="zachal"
	displayOrder=""	
	articleId="VMA_RCA_airbp-managed-events-host-os"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="RCA"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds="13185,14749,15571,15797,16080,16215,16454,16470,16802"
	cloudEnvironments="public, Fairfax, usnat, ussec, BlackForest, Mooncake"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue


<!--issueDescription-->
The physical host node where your VM was running underwent an OS Update. 

**<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. During this time RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

Azure performs updates to improve reliability, performance and security of the VMs. Azure chooses the least impactful method that might result in a brief connectivity loss. We are continuously working to improve and reduce impact of our updates and apologize for any inconvenience this may have caused you. 


<!--recommendedActions-->
## **Recommended Documents**

> Learn more about:
> * To prepare for VM maintenance events and reduce its impact, try using Scheduled Events for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) or [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) 
> * Learn more about Azure maintenance and configuring for high availability:  
>   * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) 
>   * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) 
> * Understand and use [Resource Health Center](https://docs.microsoft.com/azure/resource-health/resource-health-overview) to troubleshoot this scenario in the future 

