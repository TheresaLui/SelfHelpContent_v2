<properties
	pageTitle="I am having issues with classic metric alerts"
	description="General trouble-shooting guide for Classic metric alerts"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="8"
	articleId="insights-alert-classic-metric"
	selfHelpType="generic"
	supportTopicIds="32629619,32629626,32629633,32629639,32629645,32629657,32629663,32629676"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues with classic metric alerts

[Classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal) in Azure Monitor provide a way to get notified when a metric breaches a threshold.

## **Recommended Steps**

1. If you are trying to create a classic metric alert in Azure portal and "Add metric alerts(classic)" button is disabled, check if the resource field is selected and the resource type supports classic metric alerts
2. For a virtual machine, guest metrics are not available by default. Ensure you have [diagnostic settings enabled](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-overview) to collect guest metrics.
    
    * If you are not seeing metrics even after enabling diagnostic settings, follow the [troubleshooting steps](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-troubleshooting#metric-data-doesnt-appear-in-the-azure-portal)

3. If you believe your classic metric alert is not firing correctly, check the alert rule to verify against the metric chart

## **Recommended Documents**

* [Create, view, and manage classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal)<br>
* [Webhook payload format for classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks)<br>
