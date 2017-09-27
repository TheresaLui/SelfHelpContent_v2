<properties 
	pageTitle="My VM restarted unexpectedly"
	description="My VM restarted unexpectedly"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32411816"
	resourceTags="windows, linux, windowsSQL, redhat"	 
	productPesIds="14749"
	cloudEnvironments="MoonCake"
/>

# My VM restarted unexpectedly

## **Recommended steps**
The common reasons for a VM restarting are: Azure caused (planned or unpanned maintenance or outage), or issues with the OS or application. Use the following steps to find out the reason for a past restart and to mitigate possible future occurrences.

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) for the time period of the restart to determine the reason
2. Use 'Availability Sets' to reduce the impact of downtime events <br>
[Manage the availability of virtual machines ](https://docs.azure.cn/virtual-machines/windows/manage-availability/)

## **Recommended documents**
[Planned maintenance for Azure virtual machines](https://docs.azure.cn/virtual-machines/linux/planned-maintenance/) <br>
[View and analyze Azure Audit Logs in Power BI and more](https://azure.microsoft.com/blog/analyze-azure-audit-logs-in-powerbi-more/)
