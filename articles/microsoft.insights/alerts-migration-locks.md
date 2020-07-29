<properties
    pageTitle="Migration failed/stuck due to a policy/lock issue"
    description="Resolve migration failures due to a resource lock/policy"
    infoBubbleText=""
    service="microsoft.insights"
    resource="alertrules"
    authors="yalavi"
    ms.author="yalavi"
    displayOrder="7"
    articleId="alerts-migration-locks"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739799"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# Migration failed/stuck due to a policy/lock issue

The migration tool creates equivalent new alert rules and action groups for your classic alerts. During the migration process, it creates new alert rules and action groups and deletes the classic alerts.
If you have resource locks or policies which prevent the migration tool from creating new alerts and action groups or deleting classic alerts, migration might fail. The following steps will help you resolve the failures.

## **Recommended Steps**

1. You can find the locks or policies preventing the migration by going to [the migration start page](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/MigrationBladeViewModel).
    1. Navigate to your subscription with failures and click on **More details** link in the **Migration Details** column.
    1. This will open a blade with details of which policies or locks are causing issues.

2. [If you find a resource lock to be causing the issue](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#scope-lock-preventing-us-from-migrating-your-rules), you will need to delete the lock temporarily. Wait for a few hours as migration will be retried and add the lock back once the migration is complete.

3. If you a find a policy to be causing the issue, you will need to either edit the assignment or change the effect of the policy. [Learn how to do this](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#policy-with-deny-effect-preventing-us-from-migrating-your-rules). Wait for a few hours as migration will be retried and change the policy back to its original state after migration is complete.

4. You will need to remove any scope locks/ policies at the latest by Oct 31, 2019. If the issues are not resolved by then, accurate migration of classic alerts cannot be guaranteed.

5. If you find the migration to be stuck/failed even after a day or two after removing the locks/policy, please create a support ticket.

## **Recommended Documents**

- [Understand the automatic migration process](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-automatic-migration)
- [Understand how the migration tool works](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration)
- [Common problems with migration and how to resolve them](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-understand-migration#common-problems-and-remedies)
