<properties
  pagetitle="I am having issues trying to create, edit or delete alert rules in the Azure portal"
  service="microsoft.insights"
  resource="metricalerts"
  ms.author="harelbr,aaronmax"
  selfhelptype="Generic"
  supporttopicids="32739795"
  resourcetags=""
  productpesids="15454"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-crud-ui-metric"
  ownershipid="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts" />
# I am having issues trying to create, edit or delete alert rules in the Azure portal

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating, updating or deleting metric alert rules, then the following steps may help resolve the issue.

1. If you are looking to alert on guest metrics on virtual machines (e.g. memory, disk space), ensure you have set up diagnostic settings to send data to an Azure Monitor sink:

    * [For Windows VMs](https://docs.microsoft.com/azure/azure-monitor/platform/collect-custom-metrics-guestos-resource-manager-vm)
    * [For Linux VMs](https://docs.microsoft.com/azure/azure-monitor/platform/collect-custom-metrics-linux-telegraf)

**Note:** If you configured the guest metrics to be collected into a Log Analytics workspace, these metrics will appear under the Log Analytics workspace resource, and will start showing data **only** after creating an alert rule that monitors them. To do so, follow the steps to [configure a metric alert for logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs#configuring-metric-alert-for-logs).

2. If you cannot find metrics for a resource type, [check if the resource type is supported with metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time)

3. If you are looking to alert on a custom metric, but that metric isn't reported yet, please see how to [define an alert rule on a custom metric that isn't emitted yet](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-troubleshoot-metric#define-an-alert-rule-on-a-custom-metric-that-isnt-emitted-yet)

4. If you are looking to alert on [specific dimension values of a metric](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#using-dimensions), but cannot find these values, please note the following:

	- It might take a few minutes for the dimension values to appear under the **Dimension values** list
	- The displayed dimension values are based on metric data collected in the last three days

5. If an alert previously fired but isn't being resolved, please check the following:
	- Is the condition still met? The alert rule sends out a resolved/deactivated message when the alert condition is not met for three consecutive periods, to reduce noise in case of flapping conditions.
	- Is the alert rule configured to never resolve? Metric alert rules can be configured to never resolve, and fire an alert on every evaluation in which the alert condition is met. This can be configured when creating the alert rule programmatically (e.g. via ARM, PowerShell, REST, CLI), and setting the *autoMitigate* property to 'False'.

6. When deleting an Azure resource, associated metric alert rules aren't deleted automatically. To delete alert rules associated to a resource that has already been deleted:

	- Open the resource group in which the deleted resource was defined
	- In the list displaying the resources, check the **Show hidden types** checkbox
	- Filter the list by Type == **microsoft.insights/metricalerts**
	- Check the relevant metric alert rules and select **Delete**

7. Review if you have appropriate permissions. To create/update/delete metric alerts:

    * You should have been assigned a built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
    * You should have been assigned a [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts

### Advisory and How-To

[![Monitoring Video](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/alerts/how-to-configure-an-alert-rule.png)](https://www.microsoft.com/videoplayer/embed/RE4tflw?autoplay=1)

## **Recommended Documents**

* [How metric alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)<br>
* [Create, view, and manage metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)