<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Configuration - Host Deployment"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_NodeReboot_Host_Deployment_Config_Error"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

## **VM Availability**
<!--issueDescription-->
The Azure monitoring and diagnostics systems identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. During this time RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

<!--rcaDescription-->
### **Root Cause**
> We identified that the physical host node where the VM was running was undergoing updates for our platform components. We determined that a recent Azure deployment task inadvertently contained a configuration error when it was deployed broadly. Due to the error, the deployment failed and resulted in a number of target nodes in the cluster to become unhealthy. As a result VMs on those nodes were rebooted.
> 

<!--resolutionDetails-->
### **Resolution**
> VM was restored following reboot of the host node.
> 
> The issue was quickly detected and the ongoing deployment was stopped. Subsequent roll outs of the non-impacting update will contain a fix which resolves the issue.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> We sincerely apologize for the impact to affected customers. We are continuously improving the Microsoft Azure Platform and our processes to reduce the duration of such incidents. This includes (but is not limited to): 
> 
> - Incorporating the missed combination deployment mechanism in our validation matrix before deploying similar updates
> - Improving deployment monitoring and correlation capabilities to detect such faults and halt the rollout sooner
> 
<!--/additionalInfo-->
<!--/rcaDescription-->

<!--recommendedActions-->
## **Recommended Documents**

> *Learn more about:*
> * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates)
> * [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
> * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
> * [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
> * [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
> 
<!--/recommendedActions-->


<!--salutation-->
We apologize for any inconvenience this may have caused you. 

Microsoft Azure Team
<!--/salutation-->
