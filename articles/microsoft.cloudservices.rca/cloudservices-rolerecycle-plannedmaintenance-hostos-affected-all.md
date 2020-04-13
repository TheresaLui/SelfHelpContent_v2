<properties
	pageTitle="CloudServices RCA"
	description="RCA - Planned Maintenance - Role Recyle"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="chiragpa"
	displayOrder=""
	articleId="RoleRecycle_HostOSUpdate_All_Instances_Down"
    diagnosticScenario="CloudServiceRolecyle"
	selfHelpType="rca"
	supportTopicIds="32440212,32422590,32591241"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
## **Role Recycle incident diagnostic information** ##

Your role **<!--$RoleName-->RoleName<!--/$RoleName-->** availability has been affected from **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**  to **<!--$EndTime-->EndTime<!--/$EndTime--> (UTC)**.  The instance **<!--$ListRoleInstanceName-->ListRoleInstanceName<!--/$ListRoleInstanceName-->**  was/were down during this time frame. This expected occurrence was caused by an **Azure initiated planned maintenance action.**  

<!--/issueDescription-->

This planned maintenance update required a reboot of your Role Instance to apply the required updates to the infrastructure. The Role Instance was shut down while we patched the infrastructure, and then the Role Instance was restarted. Please note that during this patching activity we preserve the disks on your VM, so you should not have any data loss.<br> To learn more about disk partition preservation, please refer to the following article:<br>
* [Windows Azure Disk Partition Preservation](https://blogs.msdn.microsoft.com/kwill/2012/10/05/windows-azure-disk-partition-preservation/)<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you have two or more instance for each of your Web\Worker Role.<br>
To learn more about the kind of planned maintenance events that can impact the availability of your Cloud Service, their Notifications and mitigation strategy, please refer to the following articles:<br>
* [Role Instance restarts due to Planned Maintenance](https://blogs.msdn.microsoft.com/kwill/2012/09/19/role-instance-restarts-due-to-os-upgrades/)<br>

To learn more about Azure Host OS updates , please refer to the following articles:<br>
* [Windows Azure Host Updates: Why, When, and How](https://blogs.technet.microsoft.com/markrussinovich/2012/08/22/windows-azure-host-updates-why-when-and-how/)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to increase the availability of your Cloud Services.
