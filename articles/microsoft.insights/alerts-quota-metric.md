<properties
	pageTitle="I want to increase my metric alert rules quota"
	description="I want to increase my metric alert rules quota"
	infoBubbleText="Some suggestions have been found to help solve your metric alert issue more quickly"
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="1"
	articleId="alerts-quota-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739797,32739792"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I want to increase my metric alert rules quota

The number of metric alert rules per subscription is subject to the quota limits described [here](https://docs.microsoft.com/azure/azure-monitor/service-limits).

## **Recommended Steps**

If you have reached the quota limit, the following steps may help resolve the issue:

1. Try deleting or disabling metric alert rules that aren’t used anymore
2. Switch to using metric alert rules that monitor multiple resources. With this capability, a single alert rule can monitor multiple resources, with only one alert rule counted against the quota. For more information about this capability and the supported resource types, see [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#monitoring-at-scale-using-metric-alerts-in-azure-monitor).
3. If you need the quota limit to be increased, please proceed to open a support request, and provide the following information:

    - Subscription Id(s) for which the quota limit need to be increased
    - Resource type for the quota increase: **Metric Alerts** or **Metric alerts (Classic)**
    - Requested quota limit

## To check the current usage of new metric alert rules
	
### From the Azure portal

1. Open the *Alerts* screen, and click *Manage alert rules*
2. Filter to the relevant subscription using the *Subscription* dropdown control
3. Make sure NOT to filter to a specific resource group, resource type or resource
4. In the *Signal type* dropdown control, select 'Metrics'
5. Verify that the *Status* dropdown control is set to ‘Enabled’
6. The total number of metric alert rules will be displayed above the rules list

### From API

- PowerShell - [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2?view=azps-3.7.0)
- REST API - [List by subscription](https://docs.microsoft.com/rest/api/monitor/metricalerts/listbysubscription)
- Azure CLI - [az monitor metrics alert list](https://docs.microsoft.com/cli/azure/monitor/metrics/alert?view=azure-cli-latest#az-monitor-metrics-alert-list)
