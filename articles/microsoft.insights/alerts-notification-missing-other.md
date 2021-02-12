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

If you see a fired alert in the Azure portal, but its configured action did not trigger, follow these steps:

### 1. Was the action suppressed by an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)?

   To check, select the fired alert in the portal, and look at the **History** tab for suppressed [action groups](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups):

![alert details history tab with action group suppression](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/history-action-rule.png)

   If this was unintentional, modify, disable, or delete the action rule.


### 2. Did a webhook not trigger?

* **Have the source IP addresses been blocked?**

   If so, allow list the [IP addresses](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information) that the webhook is called from.

* **Does your webhook endpoint work correctly?**

    Verify that the webhook endpoint you configured is correct and that the endpoint is working correctly. Check your webhook logs, or instrument its code so that you can  investigate (for example, log the incoming payload).

* **Are you calling Slack or Microsoft Teams?**

    Each of these endpoints expects a specific JSON format. Follow [these instructions](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups-logic-app) to configure a logic app action instead.

* **Did your webhook became unresponsive or return errors?**

   Our timeout period for a webhook response is 10 seconds. The webhook call will be retried up to two additional times when the HTTP endpoint does not respond or the following HTTP status codes are returned: `408`, `429`, `503`, `504`. The first retry happens after 10 seconds. The second and final retry happens after 100 seconds. If the second retry fails, the endpoint will not be called again for 30 minutes for any action group.


### **3. Did a *secure* webhook not trigger?**

* **Did you configure the AAD correctly?**
    Follow the steps in [Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

* **Have the source IP addresses been blocked?**
   Allow list the [IP addresses](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information) that the webhook is called from.

* **Are you using correct link in the URI?**
   Check that the URI link is the correct link to the endpoint.

* **Are you trying to use Secure Export to send alerts to external systems, such as ServiceNow and BMC?**
   To configure secure webhook, follow these steps:
      1) [Register your app with Azure AD](https://docs.microsoft.com/azure/azure-monitor/platform/itsm-connector-secure-webhook-connections-azure-configuration#register-with-azure-active-directory)
      2) [Define Service principal](https://docs.microsoft.com/azure/azure-monitor/platform/itsm-connector-secure-webhook-connections-azure-configuration#define-service-principal)
      3) [Create a Secure Webhook action group](https://docs.microsoft.com/azure/azure-monitor/platform/itsm-connector-secure-webhook-connections-azure-configuration#create-a-secure-webhook-action-group)
      4) Partners configuration: At present, the configuration supports only ITOM versions of ServiceNow and BMC Helix.
         * ServiceNow ITOM [configuration](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-secure-webhook-connections-servicenow)
         * BMC Helix [configuration](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-secure-webhook-connections-bmc)
