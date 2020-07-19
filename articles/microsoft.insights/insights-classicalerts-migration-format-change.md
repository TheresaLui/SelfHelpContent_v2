<properties
	pageTitle="My action doesn’t work after migration (runbook, logic app, or webhook)"
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
	supportTopicIds="32681414"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# My action doesn’t work after migration (runbook, logic app, or webhook)

Classic alerts are being retired on August 31, 2019 and are being replaced by new alerts. Starting Sep 1, 2019, automatic migration process will be performed over few weeks. If you are having problems with actions like runbook, logic app or webhook, following steps might help resolve those.

1. The migration tool converts classic alerts into equivalent new alerts and action groups. As new alert rules support more functionality than classic alert rules, **the notification payloads for both are different**. Learn more about the [notification payload differences between classic and new alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration#notification-payload-changes).

2. If your webhooks, Logic Apps or Run books triggered by migrated alerts are not functioning correctly, ensure they can consume the new payloads. See [samples to consume the new payloads](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration#modify-a-logic-app-to-receive-a-metric-alert-notification).

## **Recommended Documents**

- [Understand the automatic migration process](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-automatic-migration)
- [Prepare your logic apps and runbooks for migration of classic alert rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration)
- [Classic alerts retirement announcement](https://docs.microsoft.com/azure/azure-monitor/platform/monitoring-classic-retirement)