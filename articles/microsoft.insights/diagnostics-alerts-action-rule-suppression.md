<properties
pageTitle="Alerts notification failure - alert possibly suppressed by action rule"
description="Alerts notification failure - alert possibly suppressed by action rule"
infoBubbleText="Possible reasons for not getting notifications on your fired alerts."
service="microsoft.insights"
resource="alerts"
authors="yagil"
ms.author="yagil"
displayOrder=""
articleId="alerts-diagnostic-notification-actionrule-supression"
diagnosticScenario="ApplicationInsightsMissingDataDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32739779,32739780,32739781,32739782"
productPesIds="15454"
cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# Alerts notification failure - alert possibly suppressed by action rule

## **Alerts notification failure - alert possibly suppressed by action rule**

<!--issueDescription-->
Our diagnostics has detected that your alert may have been suppressed by action rule <!--$ActionRuleName-->[ActionRuleName]<!--/$ActionRuleName-->. This can be a potential reason for not receiving the notification for the fired alert.
<!--/issueDescription-->

## **Recommended Steps**

**Did the action rule act on your alert?**

Check if the action rule has processed your alert by clicking on the fired alert in the portal, and look at the history tab. 

Here is an example of action rule suppressing all action groups:

![Alert details history with action rule suppression](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/history-action-rule.png)


**Does the action rule scope and filter match the fired alert?**

If you think the action rule shouldn't have suppressed your alert but it did, carefully examine the action rule scope and filter conditions versus the properties of the fired alert. 


## **Recommended Documents**

* [Azure alerts action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules?tabs=portal)
