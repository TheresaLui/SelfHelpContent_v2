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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
## **Role Recycle incident diagnostic information** ##

We attempt to start **<!--$ListRoleInstanceName-->ListRoleInstanceName<!--/$ListRoleInstanceName-->** instance of your role **<!--$RoleName-->RoleName<!--/$RoleName-->** last at  **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**  but it failed. 
We ran diagnostic on your resource and found that the **Startup task <!--$StartupTaskName-->StartupTaskName<!--/$StartupTaskName--> is exiting with nonzero error level** which is blocking the Role to be in Ready state. 
To learn more about this problem and how to troubleshoot it please refer to the following link.
[Role Recycling due to error in Startup task](https://blogs.msdn.microsoft.com/kwill/2013/08/26/troubleshooting-scenario-2-role-recycling-after-running-fine-for-2-weeks/).<br>
<!--/issueDescription-->

Startup tasks are actions that are taken before your roles begin and are defined in the ServiceDefinition.csdef file by using the Task element within the Startup element. Startup tasks can also be executed several times between reboots. For example, the startup task will be run each time the role recycles, and role recycles may not always include a reboot. Startup tasks must end with an errorlevel (or exit code) of zero for the startup process to complete. If a startup task ends with a non-zero errorlevel, the role will not start.<br>

To learn more about the order in which Startup tasks get executed, please refer to the following article:<br>
* [Startup tasks execution order](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks#role-startup-order)<br>

To learn more about the attributes of the Task element :<br>
* [Description of task attributes](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks#description-of-task-attributes)<br>

To learn more about Startup Tasks, please refer to the following articles:<br>
* [Examples of Startup tasks](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks#example-of-a-startup-task)<br>
* [Commonly used Startup tasks](https://docs.microsoft.com/azure/cloud-services/cloud-services-startup-tasks-common)<br>