<properties
	pageTitle="VMA RCA"
	description="RCA - Host Agent deployment error causes VM restart for Status: 0x80190194"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_Node_Reboot_Software_Host_Deployment_Status0x80190194"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM **<!--$vmname--> Virtual machine <!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**.
<!--/issueDescription-->

We identified the physical host node where the VM was running was undergoing updates for our platform components. We determined that a recent azure deployment task inadvertently contained a configuration error when it was deployed broadly. Due to the error the deployment failed and resulted in a number of target nodes in the cluster to become unhealthy. As a result VMs on those nodes were rebooted.

The issue was quickly detected and the ongoing deployment was stopped. Subsequently roll out of the non-impacting update will contain a fix which will resolve the issue.
<br>

We sincerely apologize for the impact to affected customers. We are continuously taking steps to improve the Microsoft Azure Platform and our processes to help reduce the duration of such incidents. This includes (but is not limited to): 

- Incorporating the missed combination deployment mechanism in our validation matrix before deploying similar updates
- Improving deployment monitoring and correlation capabilities to detect such faults and halt the rollout sooner
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.
<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
