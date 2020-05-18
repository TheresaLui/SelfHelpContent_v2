<properties
    pageTitle="Migration tool general issues"
    description="Resolve classic alerts migration tool issues"
    infoBubbleText=""
    service="microsoft.insights"
    resource="alertrules"
    authors="yalavi"
    ms.author="yalavi"
    displayOrder="7"
    articleId="alerts-migration-other"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739803"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# Migration tool general issues

Classic alerts are being retired on June 30th, 2020 and are being replaced by new alerts. Starting September 1st, 2019, automatic migration process will be performed over few weeks to convert classic alerts to new alerts. If you have any issues with the migration process, following information might help you resolve those.

## **Recommended Steps**

1. [Automatic migration process](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-automatic-migration) will be performed over few weeks starting September 1, 2019. If you want to control when the migration happens, you can still use [the migration tool](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/MigrationBladeViewModel) to trigger the migration by yourself. [Learn how to use the voluntary migration tool](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-using-migration-tool).

2. If you see the migration status as **Error fetching status**, following steps might help you resolve the issue.
    1. Check if you have permissions to view the migration status. You need to at least have a **Monitoring Reader** Role at the subscription level to view the status.
    2. Check if your subscription is registered with **Microsoft.Insights** resource provider. You can resolve this by registering your subscription with Microsoft.Insights resource provider.

3. If you see the migration status stuck with **In Progress** status, click on **More details** link for the subscription. There could be a resource lock/policy preventing the migration from completing.
    1. [If you find a resource lock to be causing the issue](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#scope-lock-preventing-us-from-migrating-your-rules), you will need to delete the lock temporarily. Wait for a few hours as migration will be retried and add the lock back once the migration is complete.
    2. If you a find a policy to be causing the issue, you will need to either edit the assignment or change the effect of the policy. [Learn how to do this](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#policy-with-deny-effect-preventing-us-from-migrating-your-rules). Wait for a few hours as migration will be retried and change the policy back to its original state after migration is complete.

4. If you migrated successfully but your webhooks, Logic Apps or Run books are not running correctly, please ensure you have updated them to work with [new payload format](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-prepare-migration#notification-payload-changes).

5. Some classic alerts will not be migrated by the migration tool. [Learn more](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#classic-alert-rules-that-will-not-be-migrated).

## **Recommended Documents**

- [Understand the automatic migration process](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-automatic-migration)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [How to use the migration tool](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-using-migration-tool)
- [Classic alerts retirement announcement](https://docs.microsoft.com/azure/azure-monitor/platform/monitoring-classic-retirement)
