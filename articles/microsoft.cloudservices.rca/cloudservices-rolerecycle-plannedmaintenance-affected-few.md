<properties
	pageTitle="CloudServices RCA"
	description="RCA - Planned Maintenance - Role Recyle"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="chiragpa"
	displayOrder=""
	articleId="RoleRecycle_GuestOSUpdate_Some_Instances_Down"
    diagnosticScenario=" CloudServiceRolecyle"
	selfHelpType="rca"
	supportTopicIds="32422590"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
## **Role Recycle incident diagnostic information** ##

Your role **<!--$RoleName-->RoleName<!--/$rolename-->** availability has been partially affected from **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**  to **<!--$EndTime-->EndTime<!--/$EndTime--> (UTC)**.  The instance **<!--$ListRoleInstanceName-->ListRoleInstanceName<!--/$ListRoleInstanceName-->**  was/were down during this time frame. This expected occurrence was caused by an **Azure initiated planned maintenance action.**  

<!--/issueDescription-->

This planned maintenance update required a reimage of your Role Instance to apply the required updates to the infrastructure. The Role Instance was shut down while we patched the infrastructure, and then the Role Instance was restarted. Please note that during this patching activity while we preserve the Local Resource disk (usually C:), the Windows disk (usually D:) gets rebuilt. If you have stored any files on the Windows disk, they will get deleted during this reimage.<br> To learn more about disk partition preservation, please refer to the following article:<br>
* [Windows Azure Disk Partition Preservation](https://blogs.msdn.microsoft.com/kwill/2012/10/05/windows-azure-disk-partition-preservation/)<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you have two or more instance for each of your Web\Worker Role.<br>
To learn more about the kind of planned maintenance events that can impact the availability of your Cloud Service, their Notifications and mitigation strategy, please refer to the following articles:<br>
* [Role Instance restarts due to Planned Maintenance](https://blogs.msdn.microsoft.com/kwill/2012/09/19/role-instance-restarts-due-to-os-upgrades/)<br>

To learn more about all the past Guest OS release and their corresponding Security updated, please refer to the following articles:<br>
* [Guest OS Releases](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-update-matrix#releases)<br>
* [Security updates on Guest OS](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-msrc-releases)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to increase the availability of your Cloud Services.
