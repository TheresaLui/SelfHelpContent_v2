<properties
pageTitle="Alerts notification failure – no fired alerts"
description="Alerts notification failure – mo fired alerts"
infoBubbleText="Possible reasons for not getting notifications on your fired alerts."
service="microsoft.insights"
resource="alerts"
authors="yagil"
ms.author="yagil"
displayOrder=""
articleId="no-fired-alerts-near-problem-start-time"
diagnosticScenario="ApplicationInsightsMissingDataDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32739779,32739780,32739781,32739782"
productPesIds="15454"
cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# Alerts notification failure – no fired alerts found

## **No fired alerts found for this alert rule**

<!--issueDescription-->
Our diagnostics have detected that no alerts have been fired for alert rule <!--$AlertRuleName-->[AlertRuleName]<!--/$AlertRuleName--> between <!--$QueryStartTime-->[QueryStartTime]<!--/$QueryStartTime--> and <!--$QueryEndTime-->[QueryEndTime]<!--/$QueryEndTime-->. This may mean that the issue you are experiencing is related to the alert not firing at all, rather than being a notification issue.
<!--/issueDescription-->

## **Recommended Steps**

**Verify the alert rule name and period**

Verify that the alert rule name and period are correct and match the issue you are reporting. You can review the [fired alerts list](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) in the Azure Portal to see if this issue might have been caused by a different alert rule firing.

**Troubleshoot why the alert didn't fire**

If the alert indeed didn't fire, but you feel that it should have, use the following troubleshooting guides to determine the reason:

* [Troubleshooting Metric Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-metric)
* [Troubleshooting Log Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-log)

## **Recommended Documents**

* [Troubleshooting Metric Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-metric)
* [Troubleshooting Log Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-log)
