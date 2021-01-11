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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue


<!--issueDescription-->
We detected that the health of the physical host Hardware your VM was running on has degraded. To prevent impact to your workload, Azure initiated a memory-preserving Kernel Soft Reboot to improve the health of the Host. During this time your VM might have been paused your VMs up to 9 seconds.

**<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. During this time RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

Azure constantly monitors for health of the physical host hardware and clusters on which your VM is running. When we observe events that could cause high impact, such as a reboot caused by underlying host hardware failure, we proactively perform a mitigation action. We are continuously working to improve the quality of our hardware and platform. We apologize for any inconvenience this may have caused you. 


<!--recommendedActions-->
## **Recommended Documents**

> *Learn more about:*
> * To prepare for VM maintenance events and reduce its impact, try using Scheduled Events forWindows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events)or[Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) 
> * Learn more about Azure maintenance and configuring for high availability:  
>   * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) 
>   * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) 
> * Understand and use [Resource Health Center](https://docs.microsoft.com/azure/resource-health/resource-health-overview) to troubleshoot this scenario in the future 

