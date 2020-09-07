<properties
	pageTitle="Migration tool is not ready for my subscription"
	description="Understand why the migration tool might not be ready for your subscription"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="7"
	articleId="insights-classicalerts-migration-tool-not-ready"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32681418"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# My subscription is marked as "Not Ready for migration"

While automatic migration process for classic alerts has started on Sep 1, 2019, you can still use the voluntary migration to migrate your classic alert rules to new rules. If you see that your subscription is not in Ready for Migration state, following steps might help you.

## **Recommended Steps**

1. Check if you have necessary permissions to see the migration status. You will need to be at least a "Monitoring Reader" at the subscription level to see the migration status.

2. Check if your subscription has any classic alert rules. If you don't have any classic alert rules in the subscription, the subscription will not need migration.
    1. You can do this by going to Alerts under Azure Monitor, clicking on "View classic alerts" and selecting your subscription.

3. Check if the subscription is registered with Microsoft.Insights resource provider. If the subscription is not registered with Insights resource provider, you will not be able to see the migration status. [Register your subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services) with Microsoft.Insights to resolve this.

4. If you still see "Not Ready for Migration", please create a support ticket.

## **Recommended Documents**

- [Classic alerts retirement announcement](https://docs.microsoft.com/azure/azure-monitor/platform/monitoring-classic-retirement)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [How to use the migration tool](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-using-migration-tool)
