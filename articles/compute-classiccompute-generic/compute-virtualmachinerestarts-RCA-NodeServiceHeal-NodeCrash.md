<properties
	pageTitle="VMA RCA"
	description="RCA - Node Service Heal - Node Crash
	infoBubbleText="An RCA has been found"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scotro"
	displayOrder=""
	articleId="UnexpectedVMReboot_C9DA72E6-81B0-48D6-8CAC-1C7B2D3EAC08"
	diagnosticScenario="rca"
	selfHelpType="diagnostics"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public"
/>

#We ran diagnostics on your resource and found an issue

## **Microsoft Azure team has concluded our investigation of the reboot of your Virtual Machine [VM]<!--($vmname)-->** 

We identified that your VM became unresponsive at <dynamic time_start> and was restored at <dynamic time_end>. This occurrence was triggered by hardware issue on the physical node where the virtual machine was hosted. As designed, this resulted in an automated recovery action for your VM where it was moved to a new physical node that does not have this problem. For more details on our auto recovery process, you can refer to the below content.

To learn more about our automated recovery action please read the following article: [Auto-recovery of Virtual Machines](https://azure.microsoft.com/en-us/blog/service-healing-auto-recovery-of-virtual-machines)

## We recommend the following steps to better avoid this issue:

	•	[Manage the availability of virtual machines](https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-manage-availability)
	•	[Configure availability of virtual machines](https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-how-to-configure-availability)
	•	Understand and use Resource Health Center to troubleshoot this scenario in the future <insert link>

## **We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you.**

Regards,
Microsoft Azure Team
