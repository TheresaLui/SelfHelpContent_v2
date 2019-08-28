<properties
	pageTitle="Migration tool failed to convert my classic alert rules"
	description="Resolve classic alerts migration tool failures"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="7"
	articleId="insights-classicalerts-migration-tool-issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32634372,32634369"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public"
/>

# Migration tool failed to convert my classic alert rules

Classic alerts are being retired on August 31, 2019 and are being replaced by new alerts. Before August 31, you can use the voluntary migration tool to migrate your classic alert rules to new rules.
If you used the migration tool but ran into some issues, the following steps might help you resolve the problems

## **Recommended Steps**

1. If you see the migration status as "Ready for migration" and details as "You do not have permissions to trigger the migration", check if you have the [necessary roles to trigger the migration](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#who-can-trigger-the-migration). Request your administrator to provide required permissions or ask them to trigger the migration.
2. If you get a "Validation Failed" error, this is a temporary error. This is due to recent change made to your classic alert rules (create, update, or delete) that is not yet synced to the new system. Please check again in 2 days, the status should become "Ready for Migration" by then and you will be able to trigger the migration.
3. If you get a "Policy or scope lock preventing us from migrating your rules", it means that there are policy or scope locks in your subscription which are preventing the tool from creating new alert rules and action groups and deleting classic alerts. You will need to temporarily disable the policy/scope lock causing the issue. The migration tool will automatically retry in about 6 hours. Once migration is complete, you can re-enable the policy/scope lock.
4. If you migrated successfully but your webhooks, Logic Apps or Run books are not running correctly, please ensure you have updated them to work with [new payload format](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration#notification-payload-changes).

## **Recommended Documents**

- [Classic alerts retirement announcement](https://docs.microsoft.com/azure/azure-monitor/platform/monitoring-classic-retirement)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [How to use the migration tool](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-using-migration-tool)
