<properties
	pageTitle="Live Migration RCA"
	description="Platform Operation - Live Migration"
	infoBubbleText="Found recovery events. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="zjalexander"
	ms.author="zachal"
	displayOrder=""	
	articleId="VMA_RCA_airbp-managed-events-livemigration-platform"
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
We detected that the Health of the cluster that your VM was running on was low. To prevent impact to your workload, Azure initiated a memory-preserving Live Migration to move your VM to a healthy node. 

<!--$EventTable-->EventTable<!--/$EventTable-->
<!--/issueDescription-->

Azure constantly monitors for health of the physical host hardware and clusters on which your VM is running. When we observe events that could cause high impact, such as a Reboot caused by underlying host hardware failure, we proactively perform mitigation action. We are continuously working to improve the quality of our hardware and platform. We apologize for any inconvenience this may have caused you. 


<!--recommendedActions-->
## **Recommended Documents**

> * To prepare for VM recovery events and reduce its impact, try using Scheduled Events for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) or [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) 
> * Learn more about Azure maintenance and configuring for high availability:  
>   * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) 
>   * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) 
> * To troubleshoot this scenario in the future, see [Resource Health Center](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

