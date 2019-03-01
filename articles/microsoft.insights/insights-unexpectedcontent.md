<properties
	pageTitle="Webhook format is different from what I expected"
	description="General trouble-shooting guide for alert webhook content"
	infoBubbleText="Some suggestions have been found to help solve your alert notification issue more quickly."
	service="microsoft.insights"
	resource="metricalerts"
	authors="dkamstra, snehithm"
	ms.author="dukek,snmuvva"
	displayOrder="5"
	articleId="insights-unexpectedcontent"
	selfHelpType="generic"
	supportTopicIds="32629652,32629665,32629666,32629667,32629668,32629669,32629670,32633013"
	productPesIds="15454,15725"​
	cloudEnvironments="public, fairfax"
/>

# Webhook notification is not in the format I expected

There are various kinds of alerts in Azure Monitor and each has a different webhook payload format. Check the expected payload format for each alert type below.

The same payload format is sent when using the alerts to trigger a logic app, a runbook or an Azure function.

## **Recommended documents**

[Payload format for Activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts-webhook)<br>
[Payload format for Log alerts for both Application Insights and Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-webhook)<br>
[Payload format for Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time#payload-schema)<br>
[Payload format for Classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks)<br>

## **Recommended steps**

- If you are using webhooks to integrate with Teams/Slack, the endpoint expects the payload in a certain format which is different from what alerts provide. [Use a logic app to integrate with Teams or Slack instead](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups-logic-app).
- If you are using custom webhook payloads functionality of log alerts, webhook payload will be in the format you specified for the alert rule.
