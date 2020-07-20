<properties
	pageTitle="CloudServices RCA"
	description="Role Recycle due to bad Startup task"
	infoBubbleText="Found recent Role not in ready state. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="chiragpa"
	displayOrder=""
	articleId="RoleRecycle_BadStartupTask"
    diagnosticScenario="CloudServiceRoleRecycle"
	selfHelpType="rca"
	supportTopicIds="32422590"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# Cloud service role is continually recycling
<!--issueDescription-->

## **Role Recycle incident diagnostic information** ##

We attempted to start **<!--$ListRoleInstanceName-->ListRoleInstanceName<!--/$ListRoleInstanceName-->** instance of your Cloud Service role **<!--$RoleName-->RoleName<!--/$RoleName-->** at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**  and it failed to start.
We ran diagnostics on your resource and found that the **startup task <!--$StartupTaskName-->StartupTaskName<!--/$StartupTaskName--> is exiting with non-zero error level** which is preventing the role from reaching a ready state.

<!--/issueDescription-->
Startup tasks are actions taken before your roles begin and are defined in the ServiceDefinition.csdef file by using the \<Task\> element within the \<Startup\> element. Startup tasks must end with an errorlevel (or exit code) of zero for the startup process to complete. If a startup task ends with a non-zero errorlevel, the role will not start.<br>

To learn more about this problem and how to troubleshoot it please refer to the following article:<br>
* [Role recycling due to error in startup task](https://blogs.msdn.microsoft.com/kwill/2013/08/26/troubleshooting-scenario-2-role-recycling-after-running-fine-for-2-weeks/).<br>


To learn more about startup tasks, please refer to the following articles:<br>
* [Cloud Services startup tasks](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks)<br>
* [Commonly used startup tasks](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks-common)

To learn more about startup tasks best practices, please refer to the following article:<br>
* [Startup tasks best practices](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks-common#task-best-practices)<br>
