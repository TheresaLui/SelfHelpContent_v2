<properties
	pageTitle="My Role is Busy or Recycling"
	description="My Role is Busy or Recycling"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="2f7c511f-6fe7-4744-be5a-d459d866bca1"
	ownershipId="Compute_VirtualMachines"
/>

# My role is Busy or Recycling
A role instance may loop between **Started**, **Initializing**, **Busy**, and **Stopped**. This condition could indicate a problem with your application code, package, or configuration file. <br>

## **Recommended steps**
1. [Check the detailed error message here](data-blade:Microsoft_Azure_CloudServices.cloudServiceStatusMessageBlade.id.$resourceId) to get details about the error message. <br>

2. Check if your detailed error message matches common issues that cause roles to be **Busy** or **Recycling**: <br>
  * [Role throwing unhandled exceptions while initializing or stopping](https://blogs.msdn.microsoft.com/kwill/2013/08/20/troubleshooting-scenario-1-role-recycling/) <br>
  * [Start-up task causing a Busy state](https://blogs.msdn.microsoft.com/kwill/2013/09/06/troubleshooting-scenario-3-role-stuck-in-busy/) <br>
  * [Start-up task causing a Recycling state after running fine for some time](https://blogs.msdn.microsoft.com/kwill/2013/08/26/troubleshooting-scenario-2-role-recycling-after-running-fine-for-2-weeks/) <br>
  * [Missing runtime dependencies](https://blogs.msdn.microsoft.com/kwill/2013/10/03/troubleshooting-scenario-7-role-recycling/) <br>
  * [Failure to cleanup/delete file causing Role Recycle](https://blogs.msdn.microsoft.com/kwill/2013/09/23/troubleshooting-scenario-6-role-recycling-after-running-for-some-time/) <br>
  * [Role returns from Run method when it should block indefinitely](https://msdn.microsoft.com/library/microsoft.windowsazure.serviceruntime.roleentrypoint.run.aspx) <br>

For more information on how to troubleshoot these types of problems, see the following links:<br>

## **Recommended documents**
[Azure PaaS Compute Diagnostics Data](http://blogs.msdn.com/b/kwill/archive/2013/08/09/windows-azure-paas-compute-diagnostics-data.aspx) <br>
[Common Issues Causing Role Recycles](https://docs.azure.cn/cloud-services/cloud-services-troubleshoot-common-issues-which-cause-roles-recycle/) <br>
