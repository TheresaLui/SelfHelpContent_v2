<properties
	pageTitle="I received an unexpected notification"
	description="Troubleshooting for whether an action rule triggered an unexpected notification."
	infoBubbleText="Some suggestions have been found to help solve your alert notification issue more quickly."
	service="microsoft.insights"
	resource="Action Rules - Preview"
	authors="ananthradhakrishnan"
	ms.author="anantr"
	displayOrder="5"
	articleId="insights-action-rules-unexpected-notification"
	selfHelpType="generic"
	supportTopicIds="32641407"
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I received an unexpected notification

[Action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules) allow you to associate action groups with Azure scopes (like subscriptions, resource groups, resources). The action groups associated with an action rule, and the action groups associated with an alert rule operate independently and are not de-duplicated, possibly causing unexpected notifications. You can check if this is the case through the following steps:

* Go to the [action rules page](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules#managing-your-action-rules), and filter for the subscription that the alert was generated on
* Search through the list of action rules for any whose scope has a match with your alert. This match could be one of the following -

    * An exact match: For example, the alert and the action rule are on the same subscription
    * A subset: For example, the alert is on a subscription, and the action rule is on a resource group within the subscription
    * A superset: For example, the alert is on a resource group, and the action rule is on the subscription that contains the resource group
    * An intersection: For example, the alert is on 'VM1' and 'VM2', and the action rule is on 'VM2' and 'VM3'

* See if the alert triggered satisfies the criteria for the action rules filtered from the step above
* The next step is to see if the remaining action rules matching on the scope and filters have an action group associated with them. If yes, the action rule would have triggered the unexpected notification. You can disable the rule to prevent this from happening again.

## **Recommended Documents**

* [Action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)<br>
* [Action rules FAQ](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules#faq)<br>

