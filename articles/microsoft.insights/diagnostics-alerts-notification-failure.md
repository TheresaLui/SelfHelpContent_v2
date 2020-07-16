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
# <-- Alerts Notification Failure -->

## ** <-- Issue Description --> **
<!--issueDescription-->
 <!--$tokenname-->[Description]<!--/$tokenname-->.

## **Recommended Steps**

We identified that no action group is configured for your alert rule. 
This may be a reason for not receiving a notification or an action on your alert. 
Please see [this article](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups) for more details on configuring action groups. 
If you can see in the portal that alerts was previously fired for this alert rule, but you never received notification for such alerts from this alert rule, this may be a potential reason. 
Please note that action groups may also be added using an action rule, if you have one configured for your rule.

## **Recommended Documents**

* [Create and manage action groups in the Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups)


