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

## **No fired alerts found for this alert rules**

<!--issueDescription-->
Our diagnostics has detected that no alerts have been fired for alert rule <!--$AlertRuleName-->[AlertRuleName]<!--/$AlertRuleName--> between [8/9/2020 12:05:00 PM] and [8/11/2020 12:05:00 PM]. This may mean that the issue you are experiencing is related to the alert not firing at all, rather than a notification issue.
<!--/issueDescription-->

## **Recommended Steps**

**Verify the alert rule name and period**

Verify that the alert rule name and period are correct and match the issue your are reporting. You can review the [fired alerts list](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) in the Azure portal to see if you may be relating to another alert rule which may have fired

**Troubleshoot why the alert didn't fire**

If the alert indeed didn't fire and you believe it should, you can try to understand why the alert didn't fire. Depending on the alert type, you can use one of the following troubleshooting guides:

* [Troubleshooting Metric Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-metric)
* [Troubleshooting Log Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-log)


## **Recommended Documents**

* [Troubleshooting Metric Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-metric)
* [Troubleshooting Log Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-log)

