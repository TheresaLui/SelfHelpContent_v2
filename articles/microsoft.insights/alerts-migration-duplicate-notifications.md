<properties
    pageTitle="I am receiving duplicate notifications after migration"
    description="Troubleshoot duplicate notifications after migration"
    infoBubbleText=""
    service="microsoft.insights"
    resource="alertrules"
    authors="yalavi"
    ms.author="yalavi"
    displayOrder="7"
    articleId="alerts-migration-duplicate-notifications"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739805"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# Duplicate notifications after migration

Classic alerts are being retired on June 30th, 2020 and are being replaced by new alerts. Starting September 1st, 2019, automatic migration process will be performed over few weeks to convert classic alerts to new alerts. If you are receiving duplicate notifications after migration, following steps might help you resolve the issue.

## **Recommended Steps**

1. The migration tool creates equivalent new alert rules and action groups for classic alerts and then deletes the classic alerts. If there is a failure in deleting the classic alert rule, you might receive duplicate notifications.
2. Check the migration status from [the migration start page](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/MigrationBladeViewModel). If the status shows as **In Progress** or **Failed**, there might be resource locks or policies preventing the migration tool from deleting the classic alerts:

    1. Click on **More details** link in the migration details column to check the resource locks/policies causing the issue
    1. Resolve the issue by removing locks/ adjusting policies as described [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#scope-lock-preventing-us-from-migrating-your-rules)
    1. If the status is **In Progress**, wait for a few hours after resolving the issue for the migration tool to complete the migration
    1. If the status is **Failed**, re-trigger the migration

3. If you can't find the resource lock/policy information in the portal, please create a support ticket

## **Recommended Documents**

- [Understand the automatic migration process](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-automatic-migration)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [Common issues with migration and how to resolve them](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#common-problems-and-remedies)
