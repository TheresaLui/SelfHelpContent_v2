<properties
	pageTitle="I am having issues with Service Health Alerts"
	description="I am having issues with Service Health Alerts"
	infoBubbleText=""
	service="microsoft.insights"
	resource="activitylogalerts"
	authors="snehithm, msvijayn, dkamstra"
	authoralias="snmuvva, vinagara,dukek"
	displayOrder="8"
	articleId="insights-alert-service-health"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630725"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues with Service Health Alerts

Azure Service Health tracks the health of your Azure services in the regions where you use them. You can set up activity log alerts on Service Health events to get notified of ongoing service issues, upcoming planned maintenance, or relevant health advisories.

## **Recommended Steps**

1. While you can view Service Health events in Azure portal, you will not receive notifications unless you set up an activity log alert on Service Health events
2. If you are having trouble integrating Service Health alerts with your webhook endpoints, review the [payload format](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts-webhook#servicehealth)

3. If you believe you should have received a Service Health notification but haven't, then:

    * Review if the **Services** in your rule match the services you were expecting the notification for
    * Review if the **Regions** in your rule match the regions where you use the Azure services
    * Review if the **Event type** in your rule matches the event type of the Service Health event

4. Service health alerts does not send an alert regarding resource health events

## **Recommended Documents**

* [Create activity log alerts on service notifications](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log-service-notifications?toc=%2fazure%2fservice-health%2ftoc.json)<br>
* [Configure health notifications for existing problem management systems using a webhook](https://docs.microsoft.com/azure/service-health/service-health-alert-webhook-guide)
