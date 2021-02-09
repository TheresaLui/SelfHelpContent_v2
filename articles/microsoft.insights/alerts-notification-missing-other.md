<properties
  pagetitle="I expected another type of action to trigger, but it didn't &#xD;"
  service=""
  resource=""
  ms.author="ofmanor,yagil,nolavime"
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

**3. Did a secure webhook not trigger?**

**2.1 Did you configured the AAD correctly?**
Follow the steps in [Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

**2.2 Have the source IP addresses been blocked?**
Whitelist the [IP addresses](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information) that the webhook is called from.

**2.3 Are you using correct link in the URI **
Check that the URI link is the correct link to the endpoint.

**2.4 Are you trying to use Secure Export in order to send alerts to External systems as ServiceNow and BMC?**
In order to configure secure webhook please follow the steps:
1) [Register your app with Azure AD](https://docs.microsoft.com/azure/azure-monitor/platform/itsm-connector-secure-webhook-connections-azure-configuration#register-with-azure-active-directory)
2) [Define Service principal](https://docs.microsoft.com/azure/azure-monitor/platform/itsm-connector-secure-webhook-connections-azure-configuration#define-service-principal)
3) [Create a Secure Webhook action group](https://docs.microsoft.com/azure/azure-monitor/platform/itsm-connector-secure-webhook-connections-azure-configuration#create-a-secure-webhook-action-group)
4) Partners configuration: today the configuration supports only ITOM versions of ServiceNow and BMC Helix.
    *ServiceNow ITOM* [configuration](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-secure-webhook-connections-servicenow)
    *BMC Helix* [configuration](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-secure-webhook-connections-bmc)