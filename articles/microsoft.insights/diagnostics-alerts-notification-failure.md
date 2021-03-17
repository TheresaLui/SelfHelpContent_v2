<properties
    pageTitle="Alerts notification failure"
    description="Alerts notification failure"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="napolish"
    ms.author="napolish"
    displayOrder="8"
    articleId="28b9e583-dbcf-44d2-907f-d8d686799206"
    selfHelpType="rca"
    supportTopicIds="32739779,32739780,32739781,32739782"
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>
# Alerts notification failure – no action groups 

## Issue Description
<!--issueDescription-->
 <!--$Description-->[Description]<!--/$Description-->
<!--/issueDescription-->

## **Recommended Steps**

We identified that no action group is configured for your alert rule. This could be a reason for not receiving a notification or an action on your alerts. See [this article](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups) for more details on configuring action groups. 

If you can see in the portal that alerts were previously fired for this alert rule, but you never received notification on alerts from this alert rule, this could be the reason. Note that action groups can also be added by using an action rule, if you have one configured for your alert rule.

## **Recommended Documents**

* [Create and manage action groups in the Azure Portal](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups)
