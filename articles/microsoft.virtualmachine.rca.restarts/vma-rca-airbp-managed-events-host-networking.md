<properties
	pageTitle="Host Networking RCA"
	description="Platform Operation - Maintenance"
	infoBubbleText="Found maintenance events. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="zjalexander"
	ms.author="zachal"
	displayOrder=""	
	articleId="VMA_RCA_airbp-managed-events-host-networking"
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
The physical host node where your VM is running had a networking stack update.

<!--$EventTable-->EventTable<!--/$EventTable-->

<!--/issueDescription-->

Azure performs updates to improve reliability, performance, and security of the VMs. Azure chooses the least impactful method, which might result in a brief connectivity loss. We are continuously working to improve and reduce impact of our updates, and we apologize for any inconvenience this may have caused you. 


<!--recommendedActions-->
## **Recommended Documents**

> * To prepare for VM maintenance events and reduce its impact, try using [Scheduled Events for Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) or [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) 
> * Learn more about Azure maintenance and configuring for high availability:  
>   * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) 
>   * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) 
> * To troubleshoot this scenario in the future, see [Resource Health Center](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

