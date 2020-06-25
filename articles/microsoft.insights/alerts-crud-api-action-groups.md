
<properties
	pageTitle="I am having issues managing Action groups with API/CLI"
	description="I am having issues managing Action groups with API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="actiongroups"
	authors="dkamstra"
	ms.author="dukek"
	displayOrder="8"
	articleId="alerts-crud-api-action-groups"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739756"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public,fairfax, mooncake, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues managing action groups with ARM templates, REST API, PowerShell or CLI 

Most alerts in Azure Monitor use [Action Groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups) as the notification delivery mechanism.

## **Recommended Steps**

__Rest API or CLI__

If you are running into issues creating/updating/deleting action groups using REST API or Azure command line interface (CLI), the following steps may help resolve the issue:

1. Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/actiongroups/) to verify you are passing the all the parameters correctly
2. Review the [CLI guide](https://docs.microsoft.com/cli/azure/monitor/action-group?view=azure-cli-latest) for samples and usage


__Arm Templates__

If you are running into issues creating/updating action groups using Azure Resource Manager (ARM) templates, the following steps may help resolve the issue:

1. Review [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) list and troubleshoot accordingly
2. Review the template to ensure you are passing the all the parameters correctly

    * See [some samples](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups-create-resource-manager-template) for metric alert templates

## **Recommended Documents**

* [Action groups](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups)<br>
* [Action Groups template reference](https://docs.microsoft.com/azure/templates/microsoft.insights/2018-09-01/actiongroups)
