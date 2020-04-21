<properties
	pageTitle="worker role (paas)/application and service availability/role startup and recycling"
	description="worker role (paas)/application and service availability/role startup and recycling"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="ChiragPavecha"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32422590"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c887b1f7-c005-422d-bf7f-7a14a718c8b2"
	ownershipId="Compute_CloudServices_Content"
/>

# worker role (paas)/application and service availability/role startup and recycling

## **Recommended Steps**

A role instance may loop between **Started**, **Initializing**, **Busy**, and **Stopped**. This condition could indicate a problem with your application code, package, or configuration file.<br>

## **Recommended steps**
1. Check the detailed error message of Role Instances which are not in Ready state from the Overview blade of your Cloud Service.<br>

2. Check if your detailed error message matches common issues that cause roles to be **Busy** or **Recycling**:<br>
  * [Role throwing unhandled exceptions while initializing or stopping](https://blogs.msdn.microsoft.com/kwill/2013/08/20/troubleshooting-scenario-1-role-recycling/)<br>
  * [Start-up task causing a Busy state](https://blogs.msdn.microsoft.com/kwill/2013/09/06/troubleshooting-scenario-3-role-stuck-in-busy/)<br>
  * [Start-up task causing a Recycling state after running fine for some time](https://blogs.msdn.microsoft.com/kwill/2013/08/26/troubleshooting-scenario-2-role-recycling-after-running-fine-for-2-weeks/)<br>
  * [Missing runtime dependencies](https://blogs.msdn.microsoft.com/kwill/2013/10/03/troubleshooting-scenario-7-role-recycling/)<br>
  * [Failure to cleanup/delete file causing Role Recycle](https://blogs.msdn.microsoft.com/kwill/2013/09/23/troubleshooting-scenario-6-role-recycling-after-running-for-some-time/)<br>
  * [Role returns from Run method when it should block indefinitely](https://msdn.microsoft.com/library/microsoft.windowsazure.serviceruntime.roleentrypoint.run.aspx)<br>

For more information on how to troubleshoot these types of problems, see the following links:<br>

## **Recommended documents**

* [Common issues that cause roles to recycle](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-common-issues-which-cause-roles-recycle/)<br>
* [Common steps to troubleshoot & address Cloud Service roles that fail to start](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-roles-that-fail-start/)<br>
* [Application issues which can cause Role to recycle](https://blogs.msdn.microsoft.com/pratyay/2018/07/30/cloud-service-troubleshooting-series/)<br>
* [Troubleshoot Cloud Services common issues - role recycling & startup](http://blogs.msdn.com/b/kwill/archive/2013/08/09/windows-azure-paas-compute-diagnostics-data.aspx)<br>
* [Various ways to Debug Cloud Services](https://docs.microsoft.com/azure/vs-azure-tools-debugging-cloud-services-overview)<br>
* [Troubleshoot Cloud Service deployment problems](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-deployment-problems/)
