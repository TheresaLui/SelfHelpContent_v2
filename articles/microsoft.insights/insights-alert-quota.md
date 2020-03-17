<properties
	pageTitle="I want to increase my alerts or action groups quota"
	description="I want to increase my alerts or action groups quota"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="8"
	articleId="insights-alert-quota"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629678,32629679,32629680,32629681,32629682, 32629683,32629684"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I want to increase my alerts or action groups quota

Some Alert types and action groups have service limits as described [here](https://docs.microsoft.com/azure/azure-subscription-service-limits#monitor-limits)

## **Recommended Steps**

1. There are no limits on number of Log alerts and activity log alerts

2. Provide the following information in the problem details to ensure faster resolution:

    * Subscription Ids for which the quota limits have to be increased. If there are multiple subscriptions you need the limit increased, provide the full list.
    * Resource type for the quota increase: **Metric Alerts**, **Metric alerts (Classic)** or **Action groups**
    * To what number quota has to be increased to: For Metric Alerts and Metric Alerts(Classic), the maximum limit is 1000
