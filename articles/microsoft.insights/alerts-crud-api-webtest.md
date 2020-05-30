<properties
	pageTitle="I'm getting an error or don't know how to create or manage availability test alert rules using ARM templates, REST API, Azure CLI or PowerShell cmdlets"
	description="I'm getting an error or don't know how to create or manage availability test alert rules using ARM templates, REST API, Azure CLI or PowerShell cmdlets"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="alerts-crud-api-webtest"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739814"
	resourceTags=""
	productPesIds="15693,15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I'm getting an error or don't know how to create or manage availability test alert rules using ARM templates, REST API, Azure CLI, or PowerShell cmdlets

## **Recommended Steps**

If you are running into issues creating/updating/deleting availability test alert rules using ARM templates, REST API, PowerShell, or the Azure command line interface (CLI), the following steps may help resolve the issue.

### ARM templates

1. Review [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) and troubleshoot accordingly
2. Refer to the [ARM template example for creating an availability test alert rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-an-availability-test-along-with-a-metric-alert) to ensure you are passing the all the parameters correctly

### REST API

* Refer to the [Create or update a web test alert rule](https://docs.microsoft.com/rest/api/monitor/metricalerts/createorupdate#create-or-update-a-web-test-alert-rule) example to verify you are passing the all the parameters correctly

### General

Make sure that you have appropriate permissions. To create/update/delete availability test alert rules:

* You should have been assigned a built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
* You should have been assigned a [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts
