<properties
	pageTitle="I am having issues managing classic metric alerts using ARM templates, REST API, PowerShell or CLI"
	description="I am having issues managing classic metric alerts using ARM templates, REST API, PowerShell or CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="alerts-crud-api-metric-classic"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739791"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I am having issues managing classic metric alerts using ARM templates, REST API, PowerShell, or CLI

[Classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating/deleting classic metric alerts using ARM templates, REST API, PowerShell, or the Azure command line interface (CLI), the following steps may help resolve the issue.

### ARM templates

* Review [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) list and troubleshoot accordingly
* Refer to the [classic metric alerts ARM template examples](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-enable-template) to ensure you are passing the all the parameters correctly

### REST API

* Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/alertrules) to verify you are passing the all the parameters correctly

### PowerShell

Ensure you are using the right PowerShell cmdlets for classic metric alerts:

* PowerShell cmdlets for classic metric alerts are available in the [Az.Monitor module](https://docs.microsoft.com/powershell/module/az.monitor/?view=azps-3.6.1)
* Make sure to use the cmdlets that **aren't** ending with V2, as those are for new (non-classic) metric alerts (e.g. to create a classic metric alert rule, use [Add-AzMetricAlertRule](https://docs.microsoft.com/powershell/module/az.monitor/Add-AzMetricAlertRule?view=azps-3.6.1))
	
### CLI

Ensure you are using the right CLI commands for metric alerts:

* CLI commands for classic metric alerts start with `az monitor alert`. Review the [Azure CLI reference](https://docs.microsoft.com/cli/azure/monitor/alert?view=azure-cli-latest) to learn about the syntax.
