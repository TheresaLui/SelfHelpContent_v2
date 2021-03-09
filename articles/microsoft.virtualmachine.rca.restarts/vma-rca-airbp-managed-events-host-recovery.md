<properties
	pageTitle="Host OS RCA"
	description="Platform Operation - Recovery"
	infoBubbleText="Found recovery events. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="zjalexander"
	ms.author="zachal"
	displayOrder=""	
	articleId="VMA_RCA_airbp-managed-events-host-recovery"
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
We detected that the health of the physical host hardware your VM runs on has degraded. To prevent impact to your workload, Azure initiated a memory-preserving Kernel Soft Reboot to improve the health of the host. 

<!--$EventTable-->EventTable<!--/$EventTable-->
<!--/issueDescription-->

Azure constantly monitors the health of the physical host hardware and clusters on which your VM runs. When we observe events that could cause high impact, such as a reboot caused by underlying host hardware failure, we proactively perform a mitigation action. We are continuously working to improve the quality of our hardware and platform, and we apologize for any inconvenience this may have caused you. 


<!--recommendedActions-->
## **Recommended Documents**

> * To prepare for VM maintenance events and reduce its impact, try using Scheduled Events for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) or [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) 
> * Learn more about Azure maintenance and configuring for high availability:  
>   * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) 
>   * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) 
> * To troubleshoot this scenario in the future, see [Resource Health Center](https://docs.microsoft.com/azure/resource-health/resource-health-overview) 

