<properties
	pageTitle="My alert notification payloads changed after using migration tool"
	description="Understand why notification payloads are different after using migration tool"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="7"
	articleId="insights-classicalerts-migration-format-change"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32634374"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public"
/>

# My alert notification payloads changed after using migration tool

Classic alerts are being retired on August 31, 2019 and are being replaced by new alerts. Before August 31, you can use the voluntary migration tool to migrate your classic alert rules to new rules.

The voluntary migration tool converts classic alerts into equivalent new alerts and action groups. As new alert rules support more functionality than classic alert rules, the notification payloads for both are different.

You can learn more about the [notification payload differences between classic and new alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration#notification-payload-changes).

If your webhooks, Logic Apps or Run books triggered by migrated alerts are not functioning correctly, ensure they can consume the new payloads. See [samples to consume the new payloads](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration#modify-a-logic-app-to-receive-a-metric-alert-notification).

## **Recommended Documents**

- [Classic alerts retirement announcement](https://docs.microsoft.com/azure/azure-monitor/platform/monitoring-classic-retirement)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [How to use the migration tool](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-using-migration-tool)
