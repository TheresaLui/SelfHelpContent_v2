<properties
	pageTitle="CloudServices RCA"
	description="RCA - Planned Maintenance - Role Recyle"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="chiragpa"
	displayOrder=""
	articleId="RoleRecycle_GuestOSUpdate_All_Instances_Down"
    diagnosticScenario="CloudServiceRolecyle"
	selfHelpType="rca"
	supportTopicIds="32422590"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
## **Role Recycle incident diagnostic information** ##

Our logs show that **<!--$ListRoleInstanceName-->ListRoleInstanceName<!--/$ListRoleInstanceName-->** of your Cloud Service role **<!--$RoleName-->RoleName<!--/$RoleName-->**, was unavailable from **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**  to **<!--$EndTime-->EndTime<!--/$EndTime--> (UTC)**. This downtime was due to a planned maintenance action initiated by the Azure platform

<!--/issueDescription-->

This planned maintenance update required a reimage of your role instance to apply required updates to the Azure infrastructure. The role instance was shut down while we patched the infrastructure, and then restarted once the patching was complete. Please note that during this patching activity, while we preserve the local resource disk, (usually C:), the Windows disk (usually D:) gets rebuilt. If you have stored any files on the Windows disk, they will get deleted during this reimage.<br> To learn more about disk partition preservation, please refer to the following article:<br>
* [Windows Azure Disk Partition Preservation](https://blogs.msdn.microsoft.com/kwill/2012/10/05/windows-azure-disk-partition-preservation/)<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you have two or more instances for each of your web\worker roles.<br>
To learn more about planned maintenance events that can impact the availability of your Cloud Service, receiving notifications when these events occur, and mitigation strategies to minimize their impact on your Cloud Services, please refer to the following article:<br>
* [Role Instance restarts due to Planned Maintenance](https://blogs.msdn.microsoft.com/kwill/2012/09/19/role-instance-restarts-due-to-os-upgrades/)<br>

To learn more about all the past guest OS releases and their corresponding security updates, please refer to the following articles:<br>
* [Guest OS Releases](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-update-matrix#releases)<br>
* [Security updates on Guest OS](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-msrc-releases)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to increase the availability of your Cloud Services.
