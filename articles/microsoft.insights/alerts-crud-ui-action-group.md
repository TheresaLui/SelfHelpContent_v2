<properties
    pageTitle="Creating, editing or deleting an action group in the Azure portal"
    description="I'm trying to create, edit or delete an action group but I'm getting an error, or I don't know how to configure it"
    infoBubbleText=""
    service="microsoft.insights"
    resource="actiongroups"
    authors="dkamstra,neilghuman"
	ms.author="dukek,neghuman"
    displayOrder="1"
    articleId="alerts-crud-ui-action-group"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739778"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# Troubleshooting information for creating an Action Group

Learn about the [behavior of each action type](https://go.microsoft.com/fwlink/?linkid=827201#action-specific-information) that can be used in an Action group.

## **Recommended Steps**

### Email

* Email notifications will be sent from these email addresses: **azure-noreply@microsoft.com**,**azureemail-noreply@microsoft.com**, and **alerts-noreply@mail.windowsazure.com**

### Email Azure Resource Manager Role
* Email will be sent to the members of the **subscription's** role. Email will only be sent to Azure AD user members of the role. Email will not be sent to Azure AD groups or service principals.

### SMS

* If you need to send SMS to a country code not currently supported we recommend you use a Logic App action and configure the Logic App to use one of the connectors provided that integrates with SMS services. [An example is available from the Azure template library](https://azure.microsoft.com/resources/templates/201-alert-to-text-message-with-logic-app/).

### Voice

* If you need to make a voice call to a country code not currently supported you will need to implement a Logic App, Function or Runbook that interfaces with your voice service provider. An example using Twilio is available [here](https://github.com/jjindrich/jjazure-twilio).

### Webhook

* [Latest list of Webhook IP addresses](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#webhook)

* The timeout period for a response is 10 seconds. The webhook call will be retried a maximum of 2 times when the following HTTP status codes are returned: 408, 429, 503, 504 or the HTTP endpoint does not respond. The first retry happens after 10 seconds. The second and last retry happens after 100 seconds. If the second retry fails the endpoint will not be called again for 30 minutes for any action group.

## **Recommended Documents**

* [Creating and managing action groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups)<br>
* [Pricing information for action group notifications](https://azure.microsoft.com/pricing/details/monitor/)

[![Monitoring Video](https://docs.microsoft.com/en-us/azure/azure-monitor/learn/media/tutorial-metrics-explorer/metric-picker.png)](https://www.microsoft.com/en-us/videoplayer/embed/RE4rBZ2)