<properties
	pageTitle="I am having issues trying to create, edit or delete classic metric alert rules in the Azure portal"
	description="I'm trying to create, edit or delete a classic metric alert rule in the Azure portal, but I'm getting an error, or I don't know how to configure it"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="alerts-crud-ui-metric-classic"
	selfHelpType="generic"
	supportTopicIds="32739788,32739789,32739790"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I am having issues with classic metric alerts

[Classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal) in Azure Monitor provide a way to get notified when a metric breaches a threshold.

## **Recommended Steps**

1. If you are trying to create a classic metric alert in Azure portal and "Add metric alerts(classic)" button is disabled, check if the resource field is selected and the resource type supports classic metric alerts.
2. For a virtual machine, guest metrics are not available by default. Ensure you have [diagnostic settings enabled](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-overview) to collect guest metrics.
    
    * If you are not seeing metrics even after enabling diagnostic settings, follow the [troubleshooting steps](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-troubleshooting#metric-data-doesnt-appear-in-the-azure-portal)

3. If you believe your classic metric alert is not firing correctly, check the alert rule to verify against the metric chart.

## **Recommended Documents**

* [Create, view, and manage classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal)
* [Webhook payload format for classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks)
