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
	supportTopicIds="32634373,32634370"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public"
/>

# My subscription is marked as "Not Ready for migration"

Classic alerts are being retired on August 31, 2019 and are being replaced by new alerts. Before August 31, you can use the voluntary migration tool to migrate your classic alert rules to new rules.

## **Recommended Steps**

1. The migration tool is rolling out in phases to all subscriptions that have classic alerts
2. Currently only subscriptions having classic alert rules on following resource types are marked as "Not Ready for Migration":

    - Classic cloud services (Microsoft.ClassicCompute/domainNames/slots/roles)
    - Cosmos DB (Microsoft.DocumentDB/databaseAccounts)
    - and some Application Insights resources

3. Check if your subscription has any classic alert rules on above resources. If so, these subscriptions will be made ready in coming weeks.

## **Recommended Documents**

- [Classic alerts retirement announcement](https://docs.microsoft.com/azure/azure-monitor/platform/monitoring-classic-retirement)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [How to use the migration tool](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-using-migration-tool)

