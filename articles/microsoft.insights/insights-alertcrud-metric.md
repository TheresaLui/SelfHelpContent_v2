<properties
	pageTitle="I am having issues creating, updating or deleting Metric alerts"
	description="I am having issues creating, updating or deleting Metric alerts"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="insights-alertcrud-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629625,32629675"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues creating, updating or deleting Metric alerts

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating or deleting metric alerts the following steps may help resolve the issue.

1. If you are looking to alert on guest metrics on virtual machines (e.g. memory, disk space), ensure you have set up diagnostic settings to send data to an Azure Monitor sink:

    * [For Windows VMs](https://docs.microsoft.com/azure/azure-monitor/platform/collect-custom-metrics-guestos-resource-manager-vm)
    * [For Linux VMs](https://docs.microsoft.com/azure/azure-monitor/platform/collect-custom-metrics-linux-telegraf)

**Note:** If you configured the guest metrics to be collected into a Log Analytics workspace, these metrics will appear under the Log Analytics workspace resource, and will start showing data **only** after creating an alert rule that monitors them. To do so, follow the steps to [configure a metric alert for logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs#configuring-metric-alert-for-logs).

2. If you cannot find metrics for a resource type, [check if the resource type is supported with metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time)

3. If you are looking to alert on a custom metric, make sure that the metric is already being reported, as you cannot define an alert rule on a custom metric that doesn't yet exist

4. If you are looking to alert on [specific dimension values of a metric](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#using-dimensions), but cannot find these values, please note the following:

	- It might take a few minutes for the dimension values to appear under the **Dimension values** list
	- The displayed dimension values are based on metric data collected in the last three days

5. If an alert previously fired but isn't being resolved, check the following:
	- Is the condition still met? The alert rule sends out a resolved/deactivated message when the alert condition is not met for three consecutive periods, to reduce noise in case of flapping conditions.
	- Is the alert rule configured to never resolve? Metric alert rules can be configured to never resolve, and fire an alert on every evaluation in which the alert condition is met. This can be configured when creating the alert rule programmatically (e.g. via ARM, PowerShell, REST, CLI), and setting the *autoMitigate* property to 'False'.

6. If you are looking to add, edit or delete tags, currently metric alert rules only support adding tags when creating a new alert rule from PowerShell or via an ARM template. Editing, removing or adding tags to an existing alert rule is currently not supported.

7. When deleting an Azure resource, associated metric alert rules aren't deleted automatically. To delete alert rules associated to a resource that has already been deleted:

	- Open the resource group in which the deleted resource was defined
	- In the list displaying the resources, check the **Show hidden types** checkbox
	- Filter the list by Type == **microsoft.insights/metricalerts**
	- Check the relevant metric alert rules and select **Delete**

8. Review if you have appropriate permissions. To create/update/delete metric alerts:

    * You should have been assigned a built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
    * You should have been assigned a [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts

## **Recommended Documents**

* [How metric alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)<br>
* [Create, view, and manage metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)
