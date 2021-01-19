<properties
  pagetitle="I expected another type of action to trigger, but it didn't &#xD;"
  service=""
  resource=""
  ms.author="ofmanor,yagil"
  selfhelptype="Generic"
  supporttopicids="32739782,32745406"
  resourcetags=""
  productpesids="15454,15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alert-notification-missing-other"
  ownershipid="AzureMonitoring_ActionGroup" />
# I expected another type of action to trigger, but it didn't 

## **Recommended Steps**

If you can see a fired alert in the portal, but its configured action did not trigger, follow these steps:

**1. Was the action suppressed by an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)?**

Check by clicking on the fired alert in the portal, and look at the history tab for suppressed [action groups](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups):

![alert details history tab with action group suppression](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/history-action-rule.png)

If that was unintentional, you can modify, disable, or delete the action rule.

**2. Did a webhook not trigger?**

**2.1 Have the source IP addresses been blocked?**

Whitelist the [IP addresses](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information) that the webhook is called from.

**2.2 Does your webhook endpoint work correctly?**

Verify the webhook endpoint you have configured is correct and the endpoint is working correctly. Check your webhook logs or instrument its code so you could investigate (for example, log the incoming payload).

**2.3 Are you calling Slack or Microsoft Teams?**

Each of these endpoints expects a specific JSON format. Follow [these instructions](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups-logic-app) to configure a logic app action instead.

**2.4 Did your webhook became unresponsive or returned errors?**

Our timeout period for a webhook response is 10 seconds. The webhook call will be retried up to two additional times when the following HTTP status codes are returned: 408, 429, 503, 504, or when the HTTP endpoint does not respond. The first retry happens after 10 seconds. The second and final retry happens after 100 seconds. If the second retry fails, the endpoint will not be called again for 30 minutes for any action group.