<properties
	pageTitle="Not all classic alerts in my subscription have been migrated"
	description="Understand why some classic alerts are not migrated using the migration tool"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="7"
	articleId="insights-classicalerts-migration-tool-alerts-not-migrated"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32681416"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# Why are some of my classic alerts not migrated

The migration tool creates equivalent new alert rules and action groups for your classic alerts. While most classic alerts are will be migrated using the migration tool, some might not be. The following information might help you understand why.

## **Recommended Steps**

1. Activity log alerts (including Service Health alerts) are already available in the new alerts and will not need to be migrated. Only classic alert rules that will need migration are
    1. Classic metric alerts (including Application Insights classic metric alerts)
    1. Application Insights classic availability test alerts
    1. Application Insights classic Failure Anomalies alerts

2. Amongst above classic alert types, some classic alerts are not migrate-able by design using the migration tool. 
    1. These could be due equivalent metrics not yet being supported in new alerts or mapping them to a single new alert rule not being possible. [See the list here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#classic-alert-rules-that-will-not-be-migrated). These are not migrated by design and will continue to function till June 2020.
    1. Some classic alerts are on target resources that have been deleted or on [deprecated metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#classic-alert-rules-on-deprecated-metrics). As these classic alerts are considered invalid, these rules will not be migrated and will be removed once automatic migration is complete for all customers.
    1. You can check if you have any rules in this category by downloading the migration details csv file and checking if you have any rules with Migratable/Migrated column as **No**

3. If you see any other failures, there might be resource locks or policies preventing the migration tool from making the required changes. [Learn how to resolve them](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#scope-lock-preventing-us-from-migrating-your-rules).

## **Recommended Documents**

- [Understand the automatic migration process](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-automatic-migration)
- [Classic alert rules that will not be migrated](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#classic-alert-rules-that-will-not-be-migrated)
- [Common problems with migration and how to resolve them](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#common-problems-and-remedies)
