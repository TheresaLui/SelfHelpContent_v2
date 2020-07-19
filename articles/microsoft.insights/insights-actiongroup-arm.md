<properties
	pageTitle="I am having issues with Action groups ARM templates"
	description="I am having issues with Action groups ARM templates"
	infoBubbleText=""
	service="microsoft.insights"
	resource="actiongroups"
	authors="snehithm,dkamstra"
	ms.author="snmuvva,dukek"
	displayOrder="8"
	articleId="insights-actiongroup-arm"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629628"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues with Action groups ARM templates

Most alerts in Azure Monitor use [Action Groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups) as the notification delivery mechanism.

## **Recommended Steps**

If you are running into issues creating/updating action groups using Azure Resource Manager (ARM) templates, the following steps may help resolve the issue:

1. Review [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) list and troubleshoot accordingly
2. Review the template to ensure you are passing the all the parameters correctly

    * See [some samples](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups-create-resource-manager-template) for metric alert templates

## **Recommended Documents**

* [Action groups](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups)<br>
* [Action Groups template reference](https://docs.microsoft.com/azure/templates/microsoft.insights/2018-09-01/actiongroups)
