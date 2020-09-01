<properties
	pageTitle="VMA RCA"
	description="RCA - Host Agent deployment error causes VM restart"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_Node_Reboot_Software_Host_Deployment_Related"
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
We identified that your VM **<!--$vmname--> Virtual machine <!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated host node reboot action**.
<!--/issueDescription-->

We identified the VM was impacted due to a recent platform deployment of Azure components. The physical node where the VM was running was impacted.  The ongoing deployment was stopped and the issue was mitigated.  Our core platform engineers are actively working on a solution for this issue.  Azure continually monitors all deployments for negative impact, and we are currently working to improve fidelity and response time to catch issues sooner.
<br>

We sincerely apologize for the impact to affected customers. We are continuously taking steps to improve the Microsoft Azure Platform and our processes to help reduce the duration of such incidents. This includes (but is not limited to): 

- Incorporating the missed combination deployment mechanism in our validation matrix before deploying similar updates
- Improving deployment monitoring and correlation capabilities to detect such faults and halt the rollout sooner
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.
<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
