<properties
	pageTitle="I am having problems creating my Action Group"
	description="General trouble-shooting guide for creating Action Groups"
	infoBubbleText=""
	service="microsoft.insights"
	resource="actiongroups"
	authors="dkamstra, snehithm"
	ms.author="dukek, snmuvva"
	displayOrder="8"
	articleId="insights-creating-action-group"
	selfHelpType="generic"
	supportTopicIds="32629621"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake"
/>

# Troubleshooting information for creating an Action Group

Learn about the [behavior of each action type](https://go.microsoft.com/fwlink/?linkid=827201#action-specific-information) that can be used in an Action group.

## **Recommended Steps**

### Email

* Email notifications will be sent from these email addresses: **azure-noreply@microsoft.com**,**azureemail-noreply@microsoft.com**, and **alerts-noreply@mail.windowsazure.com**

### SMS

* If you need to send SMS to a country code not currently supported we recommend you use a LogicApp action and configure the LogicApp to use one of the connectors provided that integrates with SMS services. See [an example from the Azure template library](https://azure.microsoft.com/resources/templates/201-alert-to-text-message-with-logic-app/).

### Voice

* If you need to make a voice call to a country code not currently supported you will need to implement a LogicApp, Function or Runbook that interfaces with your voice service provider. An example using Twilio is available here: https://github.com/jjindrich/jjazure-twilio.

### Webhook

* Webhook end points will be called from:
  * 13.106.57.181
  * 13.106.54.3
  * 13.106.54.19
  * 13.106.38.142
  * 13.106.38.148
  * 13.106.57.196

* The timeout period for a response is 10 seconds. The webhook call will be retried a maximum of 2 times when the following HTTP status codes are returned: 408, 429, 503, 504 or the HTTP endpoint does not respond. The first retry happens after 10 seconds. The second and last retry happens after 100 seconds. If the second retry fails the endpoint will not be called again for 30 minutes for any action group.

## **Recommended Documents**

[Creating and managing action groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups)<br>
[Pricing information for action group notifications](https://azure.microsoft.com/pricing/details/monitor/)